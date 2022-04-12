<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Rimuro Family</title>
	<!-- Latest compiled and minified CSS -->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">
	<style type="text/css">
		.Cuadro_Base{
			background: url(Rimuru.jpeg);
			width: 351px;
			height: 480px;
		}
		.Cuadro_Base img{
	    filter: hue-rotate(93deg);
		}
		body{
			display: flex;
			align-items: center;
			justify-content: center;
		}
	</style>
</head>
<body>
	<div class="Cuadro_Base">
		<img src="Rimuru Base.png" id="slimo"  draggable="false">
	</div>
</body>
	<script type="text/javascript">
		function drag(event){
			console.log(event);
		}
		function beginSliding(e) {
			slider.onpointermove = slide;
			beginSliding.Start=e
			slider.setPointerCapture(e.pointerId);
		}

		function stopSliding(e) {
			slider.onpointermove = null;
			slider.releasePointerCapture(e.pointerId);
		}
		function slide(e) {
			let Distancia=Math.abs(e.clientX- beginSliding.Start.clientX)%360;
			slider.style.filter = 'hue-rotate('+Distancia+'deg)';
		}
		const slider = document.getElementById('slimo');
		slider.onpointerdown = beginSliding;
		slider.onpointerup = stopSliding;
	</script>
</html>
