<script setup>
const features = [
  {
    title: "Ефективний ПОШУК",
    text: "Premium-фільтри для вузьких категорій, локальний пріоритет (платне виділення на карті / підняття в ТОП).",
    color: "#6da8d8",
  },
  {
    title: "Швидкий та безпечний ПРОДАЖ",
    text: "Safe Checkout з заморозкою коштів, AI-генерація оголошень, Smart Pricing для оптимальної ціни.",
    color: "#72a853",
  },
  {
    title: "Залучення та утримання",
    text: "Реферальні програми, швидкий вхід через соцмережі, персональні рекомендації.",
    color: "#e26b6b",
  },
];
</script>

<template>
  <div class="product-card">
    <header>
      <h3>Можливості продукту</h3>
      <p class="tag">Функції, що підвищують монетизацію та зручність</p>
    </header>

    <section class="content">
      <ul class="features">
        <li
          v-for="item in features"
          :key="item.title"
          :style="{ borderTopColor: item.color }"
        >
          <strong>{{ item.title }}</strong>
          <div class="desc">{{ item.text }}</div>
        </li>
      </ul>
    </section>
  </div>
</template>

<style scoped>
/* стиль як на слайді «Продукт» / MVP Focus */
.product-card {
  width: min(900px, 100%);
  color: #17494b;
  text-align: left;
  margin: 0 auto;
}
.product-card header {
  text-align: center;
}
.product-card header h3 {
  margin: 0;
  font-size: 2.25rem; /* text-4xl */
  font-weight: 700;
  line-height: 1.25;
  color: #17494b;
}
.product-card .tag {
  margin: 6px 0 28px;
  color: #17494b;
  opacity: 0.75;
  font-size: 1rem;
  text-align: center;
}
.product-card .features {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}
.product-card .features li {
  margin: 0;
  padding: 16px 20px;
  border-radius: 8px;
  border-top: 4px solid;
  background-color: #f3e5c7;
  font-size: 0.95rem;
  line-height: 1.35;
}
.product-card .features strong {
  display: block;
  margin-bottom: 6px;
  font-size: 1.15rem;
}
.product-card .features .desc {
  color: #17494b;
  opacity: 0.8;
  margin-top: 6px;
}
@media (max-width: 600px) {
  .product-card .features {
    grid-template-columns: 1fr;
  }
}
</style>
