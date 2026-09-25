<script setup lang="ts"></script>

<template>
  <div class="page-container">
    <slot />
  </div>
</template>

<style scoped>
.page-container {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 120px;
  left: 0;
  padding: 40px;
  background-color: cornsilk;
}
</style>
