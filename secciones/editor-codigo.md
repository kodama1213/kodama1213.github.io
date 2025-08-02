# Editor de Código Completo

HTML, CSS y JS con vista previa.

<div style="display: flex; gap: 10px; flex-wrap: wrap;">
  <div><h4>HTML</h4><textarea id="html" rows="6" cols="40"><p>Hola mundo</p></textarea></div>
  <div><h4>CSS</h4><textarea id="css" rows="6" cols="40">p { color: red; }</textarea></div>
  <div><h4>JS</h4><textarea id="js" rows="6" cols="40">console.log('¡Hola!');</textarea></div>
</div>
<br/><button onclick="runCode()">Ejecutar</button>
<iframe id="output" style="width:100%; height:300px; border:1px solid #ccc; margin-top:10px;"></iframe>

<script>
function runCode() {
  const html = document.getElementById("html").value;
  const css = "<style>" + document.getElementById("css").value + "</style>";
  const js = "<script>" + document.getElementById("js").value + "<\/script>";
  const output = html + css + js;
  const iframe = document.getElementById("output");
  const doc = iframe.contentDocument || iframe.contentWindow.document;
  doc.open(); doc.write(output); doc.close();
}
</script>
