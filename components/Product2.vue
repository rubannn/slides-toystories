<template>
  <div class="product-card">
    <header>
      <h3>MVP Focus</h3>
      <p class="tag">Базовий функціонал та безпека локальних угод</p>
    </header>

    <section class="content">
      <ul class="features">
        <li :style="{ borderTopColor: '#6da8d8' }">
          <strong>Транзакції:</strong> «Продаж», «Обмін», «Віддам» — кнопки для
          швидкої дії.
        </li>
        <li :style="{ borderTopColor: '#72a853' }">
          <strong>Локальний пошук:</strong> інтерактивна карта, налаштування
          радіуса, фільтри.
        </li>
        <li :style="{ borderTopColor: '#e26b6b' }">
          <strong>Комунікація:</strong> внутрішній чат та фіксація місця
          зустрічі.
        </li>
        <li :style="{ borderTopColor: '#e0a83e' }">
          <strong>Безпека:</strong> закриття завершених угод, рейтинги та
          відгуки.
        </li>
        <li :style="{ borderTopColor: '#6da8d8' }">
          <strong>Монетизація:</strong> швидкий вхід (Google/Apple), реферальна
          програма, платне підняття.
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
// Presentational component
</script>

<style scoped>
.product-card {
  width: min(900px, 100%);
  color: #17494b;
  text-align: left;
  margin: 0px auto;
}
.product-card header {
  text-align: center;
}
.product-card header h3 {
  margin: 0;
  font-size: 1.6rem;
}
.product-card .tag {
  margin: 6px 0 16px;
  color: #17494b;
  opacity: 0.75;
  font-size: 1rem;
}
/* кожен елемент — окрема картка, стиль як на слайді «Проблема» */
.product-card .features {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 20px;
}
.product-card .features li {
  grid-column: span 2;
  margin: 0;
  padding: 16px 20px;
  border-radius: 8px;
  border-top: 4px solid;
  background-color: #f3e5c7;
  font-size: 0.95rem;
  line-height: 1.35;
}
.product-card .features li:nth-child(n + 4) {
  grid-column: span 3;
}
.product-card .features strong {
  display: block;
  margin-bottom: 6px;
  font-size: 1.15rem;
}
</style>
