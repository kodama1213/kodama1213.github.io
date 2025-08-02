# Gráficos con Chart.js

<canvas id="myChart" width="400" height="200"></canvas>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
const ctx = document.getElementById('myChart');
new Chart(ctx, {
  type: 'bar',
  data: {
    labels: ['Rojo', 'Azul', 'Amarillo'],
    datasets: [{
      label: 'Muestra',
      data: [12, 19, 3],
      borderWidth: 1
    }]
  },
  options: {
    scales: { y: { beginAtZero: true } }
  }
});
</script>
