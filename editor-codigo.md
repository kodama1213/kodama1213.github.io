
# Editor de Código Completo

HTML, CSS y JS con vista previa.

<style>
textarea { width: 45%; height: 100px; margin: 5px; }
iframe { width: 100%; height: 200px; border: 1px solid #ccc; margin-top: 10px; }
</style>

**HTML**  
<textarea id="html"><h1>Hola Mundo</h1></textarea>

**CSS**  
<textarea id="css">h1 { color: blue; text-align: center; }</textarea>

**JS**  
<textarea id="js">document.querySelector("h1").onclick = () => alert("¡Haz clic!");</textarea>

<br/>
<button onclick="runCode()">Ejecutar</button>

<iframe id="preview"></iframe>

<script>
  function runCode() {
    const html = document.getElementById('html').value;
    const css = '<style>' + document.getElementById('css').value + '</style>';
    const js = '<script>' + document.getElementById('js').value + '<\/script>';
    const frame = document.getElementById('preview');
    const doc = frame.contentDocument || frame.contentWindow.document;
    doc.open();
    doc.write(html + css + js);
    doc.close();
  }
</script>
