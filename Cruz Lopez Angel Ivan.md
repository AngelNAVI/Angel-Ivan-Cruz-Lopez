# Json.parse-Isan
<Cruz Lopez Angel Ivan   Sec: 2NM40>
<!DOCTYPE html>
<html>
<body>

<h2>Convert a string into a function.</h2>

<p id="demo"></p>

<script>

var text = '{"precio":"decimal","liminf":"decimal","limsup":"decimal","tasa":"decimal","fija":"decimal","isan":"decimal","calcular_isan":"function() {precio= 200000;if (precio<75098.87) {"es_nivel_1":"function() {tasa=.02;fija=0.00;liminferior=0.01;limsuperior=75098.87; return es_nivel_1;}"} else {"¿es_2?":"function() {if (precio<90118.61)) {"es_nivel_2":"function() {tasa=.05;fija=1501.96;liminferior=75098.88;limsuperior=90118.61;return es_nivel_2;}"} else {"¿es_3?":"function() {if (precio<105138.43) {"es_nivel_3":"function() {tasa=.10;fija=2252.97;liminferior=98118.62;limsuperior=105138.43;return es_nivel_3;}"} else {"¿es_4?":"function() {if (precio<135117.89) {"es_nivel_4":"function() {tasa=.15;fija=3754.94;liminferior=105138.44;limsuperior=135177.89;return es_nivel_4;}" } else {"es_nivel_5":"function() {tasa=0.17;fija=8260.86;liminferior=135177.90;limsuperior=135177.89;limsuperior=135177.89;return es_nivel_5;}"}return ¿es_4?;}"}return ¿es_3?;}"}return ¿es_2?;}"}return calcular_isan;}"}';
var obj = JSON.parse(text);
obj.calcular_isan = eval("(" + obj.calcular_isan + ")");

document.getElementById("demo").innerHTML = obj.precio + ", " + obj.calcular_isan(); 

</script>

</body>
</html>
