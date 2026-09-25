<script setup lang="ts">
import CompetitionAdvantages from "./CompetitionAdvantages.vue";
import CompetitionMatrix from "./CompetitionMatrix.vue";
</script>

<template>
  <div class="competition-container">
    <CompetitionAdvantages />
    <CompetitionMatrix />
  </div>
</template>

<style scoped>
.competition-container {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;

  align-items: center;
}
</style>