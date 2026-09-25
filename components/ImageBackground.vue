<script setup lang="ts">
withDefaults(defineProps<{
  src?: string
  blur?: number
  scale?: number
  positionY?: string
  size?: string
  offsetY?: number
}>(), {
  offsetY: 0,
  positionY: 'center',
  size: 'cover',
  blur: 2,
  scale: 1,
})
</script>

<template>
  <div class="image-background">
    <div
      class="image-background__image"
      :style="{
        backgroundImage: src ? `url(${src})` : 'none',
        backgroundPosition: `center ${positionY}`,
        backgroundSize: size,
        filter: `blur(${blur}px) saturate(0.9)`,
        transform: `translateY(${offsetY}px) scale(${scale})`,
      }"
      aria-hidden="true"
    />

    <div class="image-background__content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.image-background {
  position: absolute;
  inset: 0;
  overflow: hidden;
  isolation: isolate;
  background-color: rgba(255, 255, 255, 0.15);
}

.image-background__image {
  position: absolute;
  inset: 0;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  z-index: 0;
}

.image-background__content {
  position: relative;
  z-index: 1;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
