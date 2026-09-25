<script setup lang="ts">
const investments = [
  {
    name: "Розробка",
    percentage: 50,
    amount: "$30 000",
    description: "Web + mobile + backend, підтримка MVP",
  },
  {
    name: "Маркетинг",
    percentage: 25,
    amount: "$15 000",
    description: "Залучення перших користувачів",
  },
  {
    name: "UX / UI",
    percentage: 7.5,
    amount: "$4 500",
    description: "Дослідження та дизайн продукту",
  },
  {
    name: "Інфраструктура",
    percentage: 7.5,
    amount: "$4 500",
    description: "Сервери, API, карти, AI",
  },
  {
    name: "Модерація",
    percentage: 5,
    amount: "$3 000",
    description: "Підтримка та модерація",
  },
  {
    name: "Юридичні / операційні",
    percentage: 5,
    amount: "$3 000",
    description: "Юридичні та операційні витрати",
  },
];

const total = "$60 000";
const period = "6 місяців";
</script>

<template>
  <div class="investment">
    <div class="investment__header">
      <div>
        <p class="section__label">ІНВЕСТИЦІЇ</p>
        <h2 class="investment__total">{{ total }}</h2>
      </div>

      <div class="investment__period">
        <span>Runway</span>
        <strong>{{ period }}</strong>
      </div>
    </div>

    <div class="investment__list">
      <div
        v-for="investment in investments"
        :key="investment.name"
        class="investment__item"
      >
        <div class="investment__info">
          <div class="investment__name">
            <span>{{ investment.name }}</span>
            <strong>{{ investment.amount }}</strong>
          </div>

          <p>{{ investment.description }}</p>
        </div>

        <div class="investment__percentage">
          {{ investment.percentage }}%
        </div>
      </div>
    </div>

    <div class="investment__goal">
      <span>Мета</span>
      <strong>
        MVP → перші користувачі → перевірка CAC / LTV → масштабування
      </strong>
    </div>
  </div>
</template>

<style scoped>
.investment {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 3fr;
  gap: 24px;
}

.investment__header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 46px;
}

.section__label {
  margin: 0 0 4px;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 0.14em;
  color: #17494b;
  opacity: 0.5;
}

.investment__total {
  margin: 0;
  font-size: 32px;
  font-weight: 700;
}

.investment__period {
  display: flex;
  flex-direction: column;
  align-items: end;
  gap: 4px;
}

.investment__period span {
  font-size: 9px;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  opacity: 0.45;
}

.investment__period strong {
  font-size: 14px;
}

.investment__list {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px 32px;
}

.investment__item {
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 16px;
  padding: 12px 0;
  border-bottom: 1px solid rgb(23 73 75 / 12%);
}

.investment__name {
  display: flex;
  justify-content: space-between;
  gap: 16px;
}

.investment__name span,
.investment__name strong {
  font-size: 11px;
}

.investment__info p {
  margin: 4px 0 0;
  font-size: 8px;
  opacity: 0.55;
}

.investment__percentage {
  font-size: 12px;
  font-weight: 700;
  color: #17494b;
}

.investment__goal {
  grid-column: 2/3;
  display: flex;
  align-items: center;
  gap: 16px;
  padding-top: 8px;
}

.investment__goal span {
  font-size: 9px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: #17494b;
  opacity: 0.5;
}

.investment__goal strong {
  font-size: 10px;
}
</style>