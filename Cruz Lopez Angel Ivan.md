# Json.parse-Isan
<Cruz Lopez Angel Ivan   Sec: 2NM40>
<!DOCTYPE html>
<html>
<body>

<h2>Convert a string into a function.</h2>

<p id="demo"></p>

<script>

var text = '{ "precio" : "decimal", "liminf" : "decimal", "limsup" : "decimal", "tasa" : "decimal", "fija" : "decimal", "isan" : "decimal", "calcular_isan" : "function(){ precio = 200000; if( 75098.87 > precio) {return nivel_1;} else{ if( 90118.61 > precio) {return nivel_2;} else{ if(105138.44 > precio) {return nivel_3;} else{ if(135177.89 > precio) {return nivel_4;} else{ if( precio > 135177.89) {return nivel_5;} } } } } }"}'; 
var nivel_1 = "	<br/>tasa = 0.02; <br/>fija = 0.00; <br/>liminferior = 0.01; <br/>limsuperior = 75098.87; "; 
var nivel_2 = "	<br/>tasa = 0.05; <br/>fija = 1501.96; <br/>liminferior = 75098.88; <br/>limsuperior = 90118.62; "; 
var nivel_3 = "	<br/>tasa = 0.10; <br/>fija = 2252.97; <br/>liminferior = 90118.62; <br/>limsuperior = 105138.43; "; 
var nivel_4 = "	<br/>tasa = 0.15; <br/>fija = 3754.94; <br/>liminferior = 105138.43; <br/>limsuperior = 135177.89; "; 
var nivel_5 = "	<br/>tasa = 0.17; <br/>fija = 8260.86; <br/>liminferior = 135177.89; ";
var obj = JSON.parse(text);
obj.calcular_isan = eval("(" + obj.calcular_isan + ")");

document.getElementById("demo").innerHTML = obj.precio + ", " + obj.calcular_isan(); 

</script>l

</body>
</html>
