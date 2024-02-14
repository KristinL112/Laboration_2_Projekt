<!-- Denna del av koden använder 'script setup' för att importera komponenten HeroImage.vue -->
<script setup>
  import AboutComponent from '../components/AboutComponent.vue'
</script>

<!-- Denna del av koden utgör HTML-mallen för en sida om företaget -->
<template>
  <!-- En rubrik (h1) för att visa att detta är en sida om företaget -->
  <div class="centered">
    <h2>University facts</h2>
  </div>
  <!-- En överordnad behållare med en CSS-klass 'about' för att gruppera innehållet -->
  <div class="about">
    <!-- Använder AboutComponent-komponenten för att visa info -->
    <AboutComponent />
  </div>
</template>

<style></style>
