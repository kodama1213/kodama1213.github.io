# Editor Dinámico

<textarea id="editor" rows="5" cols="50"><h2>Nuevo bloque</h2><p>Texto desde editor</p></textarea>
<button onclick="insertar()">Insertar</button>
<div id="resultado"></div>

<script>
function insertar() {
  const html = document.getElementById("editor").value;
  const contenedor = document.getElementById("resultado");
  const div = document.createElement("div");
  div.innerHTML = html;
  contenedor.appendChild(div);
}
</script>