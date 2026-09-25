<script setup lang="ts">
</script>

<template>
  <div class="competition-matrix">
    <div class="axis-label axis-label--top">
      TOY-FOCUSED
    </div>

    <div class="axis-label axis-label--bottom">
      UNIVERSAL
    </div>

    <div class="axis-label axis-label--left">
      SALES
    </div>

    <div class="axis-label axis-label--right">
      SALES + EXCHANGE
    </div>

    <div class="axis competition-matrix__axis-x"></div>
    <div class="axis competition-matrix__axis-y"></div>

    <div class="competitor competitor--olx">
      <strong>OLX</strong>
      <span>universal marketplace</span>
    </div>

    <div class="competitor competitor--shafa">
      <strong>Shafa</strong>
      <span>consumer marketplace</span>
    </div>

    <div class="competitor competitor--toyswap">
      <strong>ToySwap.world</strong>
      <span>toy exchange</span>
    </div>

    <div class="competitor competitor--toystories">
      <strong>ToyStories</strong>
      <span>parents · toys · exchange</span>
    </div>
  </div>
</template>

<style scoped>
.competition-matrix {
  position: relative;
  width: 100%;
  height: 380px;
}

/* AXES */

.axis {
  position: absolute;
  background: #17494b;
  opacity: 0.18;
}

.competition-matrix__axis-x {
  left: 9%;
  right: 5%;
  top: 50%;
  height: 1px;
}

.competition-matrix__axis-y {
  top: 7%;
  bottom: 7%;
  left: 50%;
  width: 1px;
}

/* AXIS LABELS */

.axis-label {
  position: absolute;
  color: #17494b;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 0.12em;
  opacity: 0.45;
}

.axis-label--top {
  top: 0;
  left: 50%;
  transform: translateX(-50%);
}

.axis-label--bottom {
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
}

.axis-label--left {
  left: 0;
  top: 50%;
  transform: translate(-10%, -50%) rotate(-90deg);
}

.axis-label--right {
  right: 0;
  top: 50%;
  transform: translate(10%, -50%) rotate(90deg);
}

/* COMPETITORS */

.competitor {
  position: absolute;
  display: flex;
  flex-direction: column;
  gap: 4px;

  padding: 10px 13px;

  border: 1px solid rgba(23, 73, 75, 0.14);
  border-radius: 9px;

  background: rgba(255, 255, 255, 0.94);
  box-shadow: 0 4px 14px rgba(0, 0, 0, 0.05);

  color: #17494b;
}

.competitor strong {
  font-size: 13px;
  font-weight: 700;
}

.competitor span {
  font-size: 9px;
  opacity: 0.55;
}

/* POSITIONS */

.competitor--olx {
  left: 17%;
  top: 59%;
}

.competitor--shafa {
  left: 32%;
  top: 67%;
}

.competitor--toyswap {
  left: 55%;
  top: 59%;
}

.competitor--toystories {
  left: 63%;
  top: 23%;

  border: 1.5px solid #17494b;
  box-shadow: 0 5px 18px rgba(23, 73, 75, 0.12);
}
</style>
