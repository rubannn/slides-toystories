<script setup lang="ts"></script>

<template>
  <div class="page-container-img">
    <slot />
  </div>
</template>

<style scoped>
/* как PageContainer, но залит на весь слайд (без отступа под заголовок) */
.page-container-img {
  position: absolute;
  inset: 0;
  padding: 24px;
  background-color: cornsilk;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #17494b;
}
</style>
