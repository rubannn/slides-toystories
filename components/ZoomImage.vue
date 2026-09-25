<script setup lang="ts">
import { ref, watch, onBeforeUnmount } from 'vue'

// left/top/width/rotate/z — «свободный» режим: картинка позиционируется абсолютно
// (для коллажей с наложениями). Без них — обычный режим внутри сетки.
const props = defineProps<{
  src: string
  offset?: number
  maxHeight?: number
  left?: number
  top?: number
  width?: number
  rotate?: number
  z?: number
}>()

const free = props.left !== undefined

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
  <!-- wrapper без transform: иначе fixed-картинка привяжется к нему, а не к слайду -->
  <div
    class="zoom-cell"
    :class="{ 'zoom-cell--free': free }"
    :style="free ? {
      left: left + 'px',
      top: (top ?? 0) + 'px',
      width: (width ?? 300) + 'px',
      zIndex: zoomed ? 100 : (z ?? 1),
    } : undefined"
  >
    <img
      :src="src"
      class="zoom-img"
      :class="zoomed ? 'zoom-img--open' : 'rounded-xl shadow'"
      :style="zoomed ? undefined : free ? {
        transform: `rotate(${rotate ?? 0}deg)`,
      } : {
        maxHeight: (maxHeight ?? 400) + 'px',
        transform: `translateY(${offset ?? 0}px)`,
      }"
      @click.stop="zoomed = !zoomed"
    />
  </div>
</template>

<style scoped>
.zoom-cell--free {
  position: absolute;
}

.zoom-cell--free .zoom-img:not(.zoom-img--open) {
  transition: transform 0.2s;
}

.zoom-cell--free .zoom-img:not(.zoom-img--open):hover {
  transform: scale(1.04) !important;
}

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
