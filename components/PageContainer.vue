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
  height: calc(100% - 120px);
  top: 120px;
  left: 0;
  padding: 40px;
  background-color: cornsilk;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #17494b;
}
</style>
