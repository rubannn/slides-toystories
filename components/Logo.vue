<script setup lang="ts">
const props = withDefaults(defineProps<{
  // Расположение лого на слайде
  position?: 'top-left' | 'bottom-right'
  // Размер лого (соответствует UnoCSS/Tailwind высоте h-*)
  size?: 'sm' | 'md' | 'lg' | 'xl'
  opacity?: number
}>(), {
  position: 'top-left',
  size: 'md',
  opacity: 80,
})

const positionClass = {
  'top-left': 'left-4 top-4',
  'bottom-right': 'right-4 bottom-4',
}[props.position]

const sizeClass = {
  sm: 'h-8',
  md: 'h-16',
  lg: 'h-20',
  xl: 'h-28',
}[props.size]
</script>

<template>
  <div class="absolute z-20" :class="[positionClass]" :style="{ opacity: opacity / 100 }">
    <img src="/images/logo-goit.png" class="object-contain" :class="[sizeClass]" />
  </div>
</template>
