<script setup lang="ts">
const colors = ["#6da8d8", "#72a853", "#e26b6b", "#e0a83e"];

const members = [
  {
    name: "Ольга Фурсова",
    role: "Team-Lead",
    description:
      "Активна учасниця з сильним бажанням до роботи та розвитку. В даному проєкті виконувала роль team-lead та покривала потребу у організації зустрічей, залученості у роботу проєкту, розподілення завдань та їх виконання.",
  },
  {
    name: "Віктор Бондаренко",
    role: "Product Maneger",
    description:
      "Уважний учасник команди, який помічає деталі та звертає на них увагу усієї команди. Активно приймає участь в обговоренні та прийнятті рішень, для кращої мобільності команди.",
  },
  {
    name: "Микола Рубан",
    role: "Product Maneger",
    description:
      "'Механік' команди, який завжди готовий підлатати те, що не працює та взяти на себе складні задачі з посмішкою та впевненістю. Згладжує конфлікти та обдаровує колег веселими жартами.",
  },
  {
    name: "Сергій Сидоренко",
    role: "Product Maneger",
    description:
      "Легкий на підйом та завжди готовий до роботи член команди. Вміє знайти логічне рішення у складних ситуаціях та підбадьорити групу. Захисник цінностей команди, який відкритий до нових ідей та цілей.",
  },
];
</script>

<template>
  <div class="team__grid">
    <div
      v-for="(member, i) in members"
      :key="member.name"
      class="team__member"
      :style="{ borderTopColor: colors[i % colors.length] }"
    >
      <strong>{{ member.name }}</strong>
      <span>{{ member.role }}</span>
      <p>{{ member.description }}</p>
    </div>
  </div>
</template>

<style scoped>
.team__grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
  text-align: left;
}

/* стиль карточек как на слайде «Проблема» */
.team__member {
  padding: 20px;
  border-radius: 8px;
  border-top: 4px solid;
  background-color: #f3e5c7;
  color: #17494b;
}

.team__member strong {
  display: block;
  font-size: 20px;
}

.team__member span {
  display: block;
  margin-top: 2px;
  font-size: 13px;
  opacity: 0.75;
}

.team__member p {
  margin: 10px 0 0;
  font-size: 13px;
  line-height: 1.35;
}
</style>
