<template>
  <div class="size-market">
    <table class="market-table">
      <thead>
        <tr>
          <th>Метрика</th>
          <th>Значення</th>
          <th>Джерело</th>
        </tr>
      </thead>
      <tbody class="market-body">
        <tr>
          <td>TAM</td>
          <td>$565,8 млн</td>
          <td>Euromonitor</td>
        </tr>
        <tr>
          <td>SAM</td>
          <td>$19 млн</td>
          <td>УАІ, Gradus Research</td>
        </tr>
        <tr>
          <td>SOM</td>
          <td>$190 тис</td>
          <td>Serviceable Obtainable Market</td>
        </tr>
        <tr>
          <td>CAGR</td>
          <td>~4.5%</td>
          <td>Statista (Toys & Games Market Insights)</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
// purely presentational component
</script>

<style scoped>
.size-market {
  display: flex;
  justify-content: center;
  margin-top: 18px;
}
.market-table {
  width: min(760px, 100%);
  border-collapse: collapse;
  background: rgba(255, 255, 255, 0.02);
  color: var(--v-theme-on-surface, #111);
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.06);
  border-radius: 8px;
  overflow: hidden;
  text-align: center;
}
.market-table th,
.market-table td {
  padding: 12px 16px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.06);
  text-align: center;
}
.market-table thead th {
  background: rgba(0, 0, 0, 0.05);
  font-weight: 700;
}
.market-table tbody tr:nth-child(odd) {
  background: rgba(0, 0, 0, 0.02);
}
.market-table tbody tr:last-child td {
  border-bottom: none;
}
@media (max-width: 600px) {
  .market-table th,
  .market-table td {
    padding: 8px 10px;
    font-size: 14px;
  }
}
</style>
