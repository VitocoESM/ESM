<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Dashboard – Proyecto de Instalación</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body { padding: 2rem; background-color: #f8f9fa; }
    h1, h2 { color: #6d4c41; }
    .card { margin-top: 2rem; }
    .table thead { background-color: #d7ccc8; }
    .zone-card { background-color: #efebe9; border: 1px solid #ccc; padding: 1rem; border-radius: 8px; margin-bottom: 1rem; }
  </style>
</head>
<body>
  <div class="container">
    <h1 class="mb-4 text-center">📐 Dashboard – Proyecto ESM</h1>

    <!-- Chart: avance por columna -->
    <h2>Avance por columna vertical</h2>
    <canvas id="columnChart" height="100"></canvas>
    <script>
      new Chart(document.getElementById('columnChart'), {
        type: 'bar',
        data: {
          labels: ['Columna 1', 'Columna 2', 'Columna 3', 'Columna 4'],
          datasets: [{
            label: '% Instalado',
            data: [42, 28, 71, 53],
            backgroundColor: '#8d6e63'
          }]
        },
        options: {
          scales: {
            y: { beginAtZero: true, max: 100 }
          }
        }
      });
    </script>

    <!-- Tabla por caja -->
    <div class="card">
      <div class="card-body">
        <h2 class="card-title">📋 Control de cajas por zona</h2>
        <table class="table table-bordered">
          <thead>
            <tr>
              <th>Caja</th>
              <th>Columna</th>
              <th>Nivel</th>
              <th>ST-01</th>
              <th>ST-22</th>
              <th>ST-08</th>
              <th>Estado</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>C1–N1–A</td>
              <td>1</td>
              <td>1</td>
              <td>12</td>
              <td>18</td>
              <td>8</td>
              <td>✅ Instalado</td>
            </tr>
            <tr>
              <td>C2–N1–A</td>
              <td>2</td>
              <td>1</td>
              <td>20</td>
              <td>12</td>
              <td>6</td>
              <td>🚚 En tránsito</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>

    <!-- Checklist diario -->
    <div class="card">
      <div class="card-body">
        <h2 class="card-title">📅 Checklist de instalación diaria</h2>
        <table class="table table-sm">
          <thead class="table-light">
            <tr><th>Fecha</th><th>Zona</th><th>Cajas escaneadas</th><th>Avance</th><th>Observaciones</th></tr>
          </thead>
          <tbody>
            <tr><td>22 Jul 2025</td><td>Columna 3</td><td>5 / 6</td><td>83%</td><td>Sin incidentes</td></tr>
            <tr><td>21 Jul 2025</td><td>Columna 4</td><td>3 / 5</td><td>60%</td><td>Retraso por clima</td></tr>
          </tbody>
        </table>
      </div>
    </div>

    <!-- Tarjetas visuales por zona -->
    <h2 class="mt-5">🔍 Fichas por zona</h2>
    <div class="zone-card">
      <h5>Zona: Columna 3 – Nivel 4</h5>
      <p><strong>Caja:</strong> C3–N4–A</p>
      <p><strong>Contenido:</strong> ST-01 x12, ST-22 x20, ST-08 x6</p>
      <p><strong>Estado:</strong> ✅ Instalada – 21 Jul 2025</p>
    </div>
    <div class="zone-card">
      <h5>Zona: Columna 2 – Nivel 2</h5>
      <p><strong>Caja:</strong> C2–N2–B</p>
      <p><strong>Contenido:</strong> ST-10 x38</p>
      <p><strong>Estado:</strong> 🚧 Pendiente</p>
    </div>

    <footer class="text-center mt-5">
      <p class="text-muted">Proyecto ESM – Dashboard creado por Copilot & Victor 🧱</p>
    </footer>
  </div>
</body>
</html>
