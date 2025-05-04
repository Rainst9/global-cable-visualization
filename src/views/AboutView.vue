<template>
  <div class="about">
    <div id="lottie-container"></div>
  </div>
</template>

<script setup>
import lottie from 'lottie-web'
import { onMounted } from 'vue'
import loadingData from '@/assets/animation/loading.json'

function initLottie() {
  const container = document.getElementById('lottie-container')
  lottie.loadAnimation({
    container: container,
    // path: '../assets/animation/loading.json',
    animationData: loadingData,
    renderer: 'svg',
    loop: true,
    autoplay: true,
  })
}

onMounted(() => {
  initLottie()
})
</script>
<style>
@media (min-width: 1024px) {
  #lottie-container {
    width: 400px;
    height: 400px;
  }
}
</style>
