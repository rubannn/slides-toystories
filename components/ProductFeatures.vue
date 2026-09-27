<template>
  <div class="product-card">
    <header>
      <h3>Можливості продукту</h3>
      <p class="tag">Функції, що підвищують монетизацію та зручність</p>
    </header>

    <section class="content">
      <ol class="features">
        <li>
          <strong>Ефективний ПОШУК</strong>
          <div class="desc">
            Premium-фільтри для вузьких категорій, локальний пріоритет (платне
            виділення на карті / підняття в ТОП).
          </div>
        </li>
        <li>
          <strong>Швидкий та безпечний ПРОДАЖ</strong>
          <div class="desc">
            Safe Checkout з заморозкою коштів, AI-генерація оголошень, Smart
            Pricing для оптимальної ціни.
          </div>
        </li>
        <li>
          <strong>Залучення та утримання</strong>
          <div class="desc">
            Реферальні програми, швидкий вхід через соцмережі, персональні
            рекомендації.
          </div>
        </li>
      </ol>
    </section>
  </div>
</template>

<script setup>
// Presentational component
</script>

<style scoped>
.product-card {
  width: min(760px, 100%);
  background: #f3e5c7;
  padding: 16px;
  border-radius: 8px;
  border-top: 4px solid #6da8d8;
  color: #17494b;
  margin: 0 auto;
  text-align: center;
}
.product-card header h3 {
  margin: 0;
  font-size: 1.1rem;
}
.product-card .tag {
  margin: 6px 0 12px;
  color: rgba(0, 0, 0, 0.6);
  font-size: 0.92rem;
}
.product-card .features {
  list-style: decimal;
  padding-left: 20px;
  margin: 0;
  display: inline-block;
  text-align: left;
  max-width: 720px;
  width: 100%;
}
.product-card .features li {
  margin: 12px 0;
}
.product-card .features .desc {
  color: rgba(0, 0, 0, 0.7);
  margin-top: 6px;
}
@media (max-width: 600px) {
  .product-card {
    padding: 12px;
  }
}
</style>
