<script setup lang="ts">
const blocks = [
  {
    name: "Монетизація",
    values: [
      "Premium: $1 / місяць",
      "Premium: $10 / рік",
      "Додатково: платне просування, партнерські доходи, реклама",
      "Premium ≈ 40% структури доходів",
      "Комісія 10%",
    ],
  },
  {
    name: "Ключовий фінансовий показник",
    values: [
      "ROMI = (LTV − CAC) / CAC × 100%",
      "Основна ідея: LTV має перевищувати CAC",
      "Churn: 20–30% / міс. для місячної когорти; 50–70% / рік для річної",
      "Для базового розрахунку: 50% місячних + 50% річних підписок",
    ],
  },
];
</script>

<template>
  <div class="bmc__grid">
    <h2 class="page__title">Freemium як основа ToyStories</h2>
    <div v-for="block in blocks" class="bmc__block">
      <p class="block__title">{{ block.name }}</p>
      <ul class="values__list">
        <li v-for="value in block.values" class="block__value">{{ value }}</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.bmc__grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 34px;
}

.bmc__block {
  border: 1px solid rgba(23, 73, 75, 0.15);
  padding: 8px;
  border-radius: 9px;
  overflow: hidden;
}

.bmc__block:nth-child(2) .values__list {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 8px;
}

.bmc__block:nth-child(2) .block__value {
  border: 1px solid rgba(23, 73, 75, 0.15);
  border-radius: 9px;
  background-color: #ffce2d89;

  display: flex;
  align-items: center;
  justify-content: center;
  padding: 8px;
}

.bmc__block:nth-child(3) .values__list {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 14px;
}

.bmc__block:nth-child(3) .block__value {
  text-align: left;
  border-bottom: 2px solid #17494b19;
}

.page__title {
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 0.1em;

  grid-column: 1/3;
}

.block__title {
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.14em;
  line-height: 80%;

  color: #17494b;
  text-transform: uppercase;
}

.values__list {
  margin: 0;
  padding: 0;
  list-style: none;
}

.block__value {
  font-size: 10px;
}
</style>
