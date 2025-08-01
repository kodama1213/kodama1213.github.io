# Generador de Tarjetas

<form onsubmit="crearTarjeta(); return false;">
  <input type="text" id="titulo" placeholder="Título" required>
  <input type="text" id="contenido" placeholder="Contenido" required>
  <button type="submit">Crear</button>
</form>

<div id="tarjetas"></div>

<script>
function crearTarjeta() {
  const titulo = document.getElementById('titulo').value;
  const contenido = document.getElementById('contenido').value;
  const tarjeta = document.createElement('div');
  tarjeta.innerHTML = `<h4>${titulo}</h4><p>${contenido}</p><hr>`;
  document.getElementById('tarjetas').appendChild(tarjeta);
}
</script>