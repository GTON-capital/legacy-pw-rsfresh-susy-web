<template>
  <svg class="loader" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
    <circle cx="50" cy="50" r="45"/>
  </svg>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
})
</script>

<style lang="postcss">
.loader {
  animation: 2s linear infinite svg-animation;
  circle {
    animation: 1.4s ease-in-out infinite both circle-animation;
    display: block;
    fill: transparent;
    stroke: currentColor;
    stroke-linecap: round;
    stroke-dasharray: 283;
    stroke-dashoffset: 280;
    stroke-width: 10px;
    transform-origin: 50% 50%;
  }
}

@keyframes svg-animation {
  0% {
    transform: rotateZ(0deg);
  }
  100% {
    transform: rotateZ(360deg)
  }
}

@keyframes circle-animation {
  0%,
  25% {
    stroke-dashoffset: 280;
    transform: rotate(0);
  }

  50%,
  75% {
    stroke-dashoffset: 75;
    transform: rotate(45deg);
  }

  100% {
    stroke-dashoffset: 280;
    transform: rotate(360deg);
  }
}
</style>
