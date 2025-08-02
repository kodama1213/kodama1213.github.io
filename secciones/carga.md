# Subir y mostrar archivos (visual)

<input type="file" multiple id="fileInput" />
<ul id="fileList"></ul>

<script>
document.getElementById("fileInput").addEventListener("change", function(e) {
  const list = document.getElementById("fileList");
  list.innerHTML = "";
  for (let file of e.target.files) {
    const li = document.createElement("li");
    li.textContent = file.name;
    list.appendChild(li);
  }
});
</script>
