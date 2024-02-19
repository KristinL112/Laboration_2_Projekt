<!-- Denna del av koden använder 'script setup' för att importera komponenten HeroImage.vue -->
<script setup>
  import AboutComponent from '../components/AboutComponent.vue'
</script>

<template>
  <div>
    <AboutComponent />
  </div>
</template>

<script></script>

<style scoped>
  .header,
  p {
    padding-left: 2vh;
    padding-top: 2vh;
  }
</style>
