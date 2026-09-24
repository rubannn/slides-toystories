<script setup lang="ts">
withDefaults(defineProps<{
  text: string
  fontSize?: string
  opacity?: number
}>(), {
  fontSize: '16px',
  opacity: 80,
})
</script>

<template>
  <div
    class="person-name"
    :style="{ fontSize, opacity: opacity / 100 }"
  >
    {{ text }}
  </div>
</template>

<style scoped>
.person-name {
  position: absolute;
  left: 1rem;
  bottom: 1rem;
  z-index: 20;
  max-width: 75%;
  color: red;
  font-weight: 500;
  line-height: 1.4;
  text-align: left;
  overflow-wrap: anywhere;
}
</style>
