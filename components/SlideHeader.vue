<script setup lang="ts">
import headerImage from '../images/header.png'

withDefaults(defineProps<{
  title: string
  fontSize?: string
}>(), {
  fontSize: '26px',
})
</script>

<template>
  <header class="slide-header">
    <img :src="headerImage" alt="" class="slide-header__image" />
    <h1 class="slide-header__title" :style="{ fontSize }">{{ title }}</h1>
  </header>
</template>

<style scoped>
.slide-header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 120px;
  z-index: 10;
}

.slide-header__image {
  display: block;
  width: 100%;
  height: 100%;
}

.slide-header__title {
  position: absolute;
  left: 39%;
  right: 9%;
  top: 26%;
  height: 47%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0;
  padding: 0;
  color: #17494b;
  font-weight: 700;
  line-height: 1.15;
  text-align: center;
  overflow-wrap: anywhere;
}
</style>
