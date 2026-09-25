<template>
  <div class="product-card">
    <header>
      <h3>MVP Focus</h3>
      <p class="tag">Базовий функціонал та безпека локальних угод</p>
    </header>

    <section class="content">
      <ul class="features">
        <li>
          <strong>Транзакції:</strong> «Продаж», «Обмін», «Віддам» — кнопки для
          швидкої дії.
        </li>
        <li>
          <strong>Локальний пошук:</strong> інтерактивна карта, налаштування
          радіуса, фільтри.
        </li>
        <li>
          <strong>Комунікація:</strong> внутрішній чат та фіксація місця
          зустрічі.
        </li>
        <li>
          <strong>Безпека:</strong> закриття завершених угод, рейтинги та
          відгуки.
        </li>
        <li>
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
  width: min(760px, 100%);
  background: rgba(255, 255, 255, 0.02);
  padding: 16px;
  border-radius: 8px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.06);
  color: var(--v-theme-on-surface, #111);
  margin: 0px auto;
}
.product-card header h3 {
  margin: 0;
  font-size: 1.05rem;
}
.product-card .tag {
  margin: 6px 0 12px;
  color: rgba(0, 0, 0, 0.6);
  font-size: 0.9rem;
}
.product-card .features {
  list-style: decimal;
  padding-left: 20px;
  margin: 0;
}
.product-card .features li {
  margin: 8px 0;
}
.product-card .features {
  list-style: decimal;
  padding-left: 20px;
  margin: 0;
  display: inline-block;
  text-align: left;
  max-width: 640px;
  width: 100%;
}
</style>
