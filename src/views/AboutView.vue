<!-- Denna del av koden använder 'script setup' för att importera komponenten HeroImage.vue -->
<script setup>
  import ChildComponent from '../components/ChildComponent.vue'
  import AboutComponent from '../components/AboutComponent.vue'
</script>

<template>
  <div>
    <div class="header"><h4>University facts</h4></div>
    <AboutComponent />
    <div>
      <ChildComponent v-on:changeTitle="updateTitleText($event)" />
      <p>{{ title }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: ''
      }
    },
    name: 'AboutView',
    components: { childComponent: ChildComponent },

    methods: {
      updateTitleText(title) {
        this.title = title
      }
    }
  }
</script>

<style scoped>
  .header,
  p {
    padding-left: 2vh;
    padding-top: 2vh;
  }
</style>
