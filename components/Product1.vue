<template>
  <div class="product-card">
    <header>
      <p class="tag">Нішевий маркетплейс дитячих іграшок</p>
    </header>

    <section class="content">
      <p class="lead">
        Екологічне та економне оновлення іграшок — фокус на обміні та локальній
        взаємодії.
      </p>

      <ul class="usps">
        <li><strong>Вузький фокус:</strong> спеціалізовані дитячі фільтри.</li>
        <li><strong>Прямий бартер:</strong> обмін іграшки на іграшку.</li>
        <li><strong>Гіперлокальність:</strong> пошук у заданому радіусі.</li>
      </ul>

      <div class="personas">
        <div><strong>Свідома мама:</strong> якісні іграшки — не сміття.</div>
        <div>
          <strong>Прагматичний батько:</strong> регулярне оновлення без удару по
          бюджету.
        </div>
      </div>
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
  margin: 120px auto;
}
.product-card header h3 {
  margin: 0;
  font-size: 1.15rem;
}
.product-card .tag {
  margin: 6px 0 12px;
  color: rgba(0, 0, 0, 0.6);
  font-size: 0.92rem;
}
.product-card .lead {
  margin: 0 0 12px;
}
.product-card .usps {
  list-style: disc;
  padding-left: 20px;
  margin: 0 0 12px;
}
.product-card .usps li {
  margin: 6px 0;
}
.product-card .personas {
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-size: 0.95rem;
  color: rgba(0, 0, 0, 0.8);
}
@media (min-width: 700px) {
  .product-card .personas {
    grid-template-columns: 1fr 1fr;
  }
}
</style>
