<!-- script setup används för att importera komponenter och använda Composition API -->
<script setup>
  // Importerar komponenten HeroImage.vue och Search

  import HeroImage from '../components/HeroImage.vue'
  import SearchComponent from '../components/SearchComponent.vue'
</script>

<template>
  <main>
    <HeroImage />
    <SearchComponent />
  </main>
</template>
