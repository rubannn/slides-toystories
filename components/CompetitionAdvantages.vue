<script setup lang="ts">
const advantages = [
  {
    number: '01',
    title: 'Local map',
    description: 'Find offers near home',
  },
  {
    number: '02',
    title: 'Buy · sell · exchange',
    description: 'Several ways to reuse toys',
  },
  {
    number: '03',
    title: 'Parent-oriented filters',
    description: 'Age · category · interests',
  },
  {
    number: '04',
    title: 'AI-assisted listings',
    description: 'Description + price recommendation',
  },
]
</script>

<template>
  <section class="advantages">
    <div class="advantages__title">
      WHY TOYSTORIES?
    </div>

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
  </section>
</template>

<style scoped>
.advantages {
  height: fit-content;
  padding: 18px 22px;

  border-left: 1px solid rgba(23, 73, 75, 0.15);

  color: #17494b;
}

.advantages__title {
  margin-bottom: 20px;

  font-size: 10px;
  font-weight: 700;
  letter-spacing: 0.14em;

  opacity: 0.5;
}

.advantages__grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px 20px;
}

.advantage {
  display: flex;
  align-items: flex-start;
  gap: 9px;
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

.advantage__content strong {
  font-size: 12px;
  font-weight: 700;
}

.advantage__content span {
  font-size: 9px;
  line-height: 1.4;
  opacity: 0.55;
}
</style>
