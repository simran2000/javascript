<!DOCTYPE html>
<html>
<head>
	<title></title>
	<link rel="stylesheet" href="https://maxcdin.bootstrap.com/bootstrap/4.2.1/cs/bootstrap.min.css">

</head>
<body>
	<div class="container">
		<div class="card">
			<div class="card-header text-center"> BMI Calculator </div>
			<div class="card-body"></div>
			   <form class="w-50 m-auto" onsubmit="return false">
				  <div class="form-group">
				    <label> Weight: </label>
					<input type="number" name="" placeholder="Weight in Kg"  id="weight" class="form-control">
				</div>
				<div class="form-group">
					<label> Height: </label>
					<input type="number" name="" placeholder=" Height in Ft" id="height" class="form-control">
				</div>
				<div class="form-group">
					<label> BMI Value: </label>
					<input type="number" name="" id="bmivalue" class="form-control">
				</div>
				<div>
					<button type="submit" class="btn btn-success " onclick="getbmivalue()"> Check BMI</button>
				</div>

			   </form>

	  </div>
	     <div class="card-footer text-center">A healthy BMI ranges between 19 to 25. </div>
	</div>


	<script >
		function getbmivalue(){

		var weight = document.getElementById('weight').Value;

		var height = document.getElementById('height').value;

		height = height * 12;
		height = height * 0.025; // now height in meter;

		var newbmivalue = weight / (Math.pow(height,2));

		 newbmivalue = Math.round(newbmivalue);

		document.getElementById('bmivalue').value = newbmivalue;
        	}
	</script>
	

</body>
</html>
