<script setup lang="ts">
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
    <div v-for="member in members" class="team__member">
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
  gap: 20px;
}

.team__member {
  padding: 20px;
  border: 1px solid #17494b;
}

.team__member strong {
  display: block;
  font-size: 14px;
}

.team__member span {
  display: block;
  margin-top: 4px;
  font-size: 10px;
  color: #17494b;
}

.team__member p {
  margin: 10px 0 0;
  font-size: 9px;
}
</style>
