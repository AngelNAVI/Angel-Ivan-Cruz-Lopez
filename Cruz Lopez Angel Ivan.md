# Json.parse-Isan
<Cruz Lopez Angel Ivan   Sec: 2NM40>
<!DOCTYPE html>
<html>
<body>

<h2>Convert a string into a function.</h2>

<p id="demo"></p>

<script>

var text = '{ "isan":"function() {precio=200000; if(precio<75098.87){tasa=0.02;fija=0.00; isan=(precio*tasa)+fija;return isan} else {if(precio<90118.61){tasa=0.05;fija=1501.96; isan=(precio*tasa)+fija;return isan}else{if(precio<105138.43){tasa=0.10;fija=2252.97; isan=(precio*tasa)+fija;return isan;}else{if(precio<135117.89){tasa=0.15;fija=3754.94; isan=(precio*tasa)+fija;return isan;}else{tasa=0.17;fija=8260.86; isan=(precio*tasa)+fija;return isan}}}}}"}';

var obj = JSON.parse(text);

obj.isan = eval("(" + obj.isan + ")");

document.getElementById("demo").innerHTML = obj.precio + ", " + obj.isan(); 

</script>

</body>
</html>
