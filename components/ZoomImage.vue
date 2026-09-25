<script setup lang="ts">
import { ref, watch, onBeforeUnmount } from 'vue'

defineProps<{
  src: string
  offset?: number
  maxHeight?: number
}>()

const zoomed = ref(false)

// capture + stopPropagation, чтобы Slidev не обработал Esc сам (обзор слайдов)
function onKey(e: KeyboardEvent) {
  if (e.key === 'Escape') {
    e.stopPropagation()
    zoomed.value = false
  }
}

watch(zoomed, (open) => {
  if (open)
    window.addEventListener('keydown', onKey, true)
  else
    window.removeEventListener('keydown', onKey, true)
})

onBeforeUnmount(() => window.removeEventListener('keydown', onKey, true))
</script>

<template>
  <div class="zoom-cell">
    <img
      :src="src"
      class="zoom-img"
      :class="zoomed ? 'zoom-img--open' : 'rounded-xl shadow'"
      :style="zoomed ? undefined : {
        maxHeight: (maxHeight ?? 400) + 'px',
        transform: `translateY(${offset ?? 0}px)`,
      }"
      @click.stop="zoomed = !zoomed"
    />
  </div>
</template>

<style scoped>
.zoom-img {
  width: 100%;
  object-fit: contain;
  cursor: zoom-in;
}

/* fixed внутри слайда (у него есть transform) — занимает весь слайд */
.zoom-img--open {
  position: fixed;
  inset: 0;
  width: 100%;
  height: 100%;
  z-index: 100;
  padding: 16px;
  background: rgba(0, 0, 0, 0.85);
  backdrop-filter: blur(6px);
  cursor: zoom-out;
  animation: zoom-flip 0.5s cubic-bezier(0.34, 1.56, 0.64, 1);
}

/* 3D-переворот с «пружинкой» в конце */
@keyframes zoom-flip {
  from {
    opacity: 0;
    transform: perspective(1200px) rotateY(-90deg) scale(0.5);
  }
  60% {
    opacity: 1;
  }
  to {
    opacity: 1;
    transform: perspective(1200px) rotateY(0) scale(1);
  }
}
</style>
