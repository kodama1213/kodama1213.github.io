# 🧩 Editor de Código HTML

<textarea id="editor" rows="6" cols="60">
<h3>Sección dinámica</h3>
<p>Texto generado desde el navegador.</p>
</textarea><br>
<button onclick="insertar()">Insertar en la página</button>

<div id="resultado" style="margin-top:20px;"></div>

<script>
function insertar() {
  const html = document.getElementById("editor").value;
  const contenedor = document.getElementById("resultado");
  const div = document.createElement("div");
  div.innerHTML = html;
  contenedor.appendChild(div);
}
</script>
