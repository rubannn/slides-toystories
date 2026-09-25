<script setup lang="ts">
const advantages = [
  {
    number: "01",
    title: "Local map",
    description: "Find offers near home",
  },
  {
    number: "02",
    title: "Buy · sell · exchange · donate",
    description: "Several ways to reuse toys",
  },
  {
    number: "03",
    title: "Parent-oriented filters",
    description: "Age · category · interests",
  },
  {
    number: "04",
    title: "AI-assisted listings",
    description: "Description + price recommendation",
  },
];

const competitors = [
  {
    name: "OLX",
    values: [
      "Large scale & selection",
      "Strong brand recognition",
      "Sales of children's products",
      "Lacks a narrow focus on parents' needs",
    ],
  },
  {
    name: "Shafa",
    values: [
      "A developed marketplace",
      "Search, ratings, secure payment and delivery",
      "Paid promotion",
      "Broader focus than just children's products",
    ],
  },
  {
    name: "ToySwap.world",
    values: [
      "Closest direct competitor",
      "Buying, selling, exchanging and donating toys",
      "Specialization in toys",
      "Smaller audience and number of offers",
    ],
  },
];
</script>

<template>
  <section class="advantages">
    <div class="advantages__container">
      <p2 class="advantages__title"> Why ToyStories? </p2>

      <div class="advantages__grid">
        <article
          v-for="advantage in advantages"
          :key="advantage.number"
          class="advantage"
        >
          <span class="advantage__number">
            {{ advantage.number }}
          </span>

          <div class="advantage__content">
            <strong>{{ advantage.title }}</strong>
            <span>{{ advantage.description }}</span>
          </div>
        </article>
      </div>
    </div>

    <div class="advantages__container">
      <p2 class="advantages__title">Competitors</p2>

      <div class="competitors__list">
        <div
          v-for="competitor in competitors"
          :key="competitor.name"
          class="competitors__box"
        >
          <strong class="competitor__name">{{ competitor.name }}</strong>
          <ul class="values__list">
            <li
              v-for="value in competitor.values"
              :key="value"
              class="competitor__value"
            >
              {{ value }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.advantages {
  height: 100%;

  display: flex;
  flex-direction: column;
  gap: 24px;

  border-left: 1px solid rgba(23, 73, 75, 0.15);

  color: #17494b;
}

.advantages__container {
  padding: 0 12px;
}

.competitors__list {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

.values__list {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  list-style: none;
  gap: 8px;
  margin: 0;
  padding: 0;
}

.competitor__value {
  font-size: 8px;
  padding: 0;
  margin: 0;
}

.advantages__title {
  margin-bottom: 20px;

  font-size: 10px;
  font-weight: 700;
  letter-spacing: 0.14em;
  text-transform: uppercase;

  opacity: 0.5;
}

.advantages__grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 24px 20px;
}

.advantage {
  display: flex;
  align-items: flex-start;
  gap: 9px;
  padding: 6px;
  border: 1px solid #ffce2d;
  border-radius: 9px;
}

.advantage__number {
  padding-top: 2px;

  font-size: 9px;
  font-weight: 700;

  opacity: 0.35;
}

.advantage__content {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.competitor__name,
.advantage__content strong {
  font-size: 12px;
  font-weight: 700;
}

.competitor__value,
.advantage__content span {
  font-size: 9px;
  line-height: 1.4;
  opacity: 0.55;
}
</style>
