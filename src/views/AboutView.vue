<!-- Denna del av koden använder 'script setup' för att importera komponenten HeroImage.vue -->
<script setup>
  import ChildComponent from '../components/ChildComponent.vue'
  import AboutComponent from '../components/AboutComponent.vue'
</script>

<template>
  <div>
    <div>
      <h1>{{ title }}</h1>
      <ChildComponent v-on:changeTitle="updateTitleText($event)" />
    </div>
    <div class="header"><h4>University facts</h4></div>
  </div>
  <ChildComponent />
  <AboutComponent />
</template>

<style scoped>
  .header,
  p {
    padding-left: 2vh;
    padding-top: 2vh;
  }
</style>

<script>
  export default {
      data() {
        return {
          title: 'Child to parent Data'
        }
      },
      name: 'AboutView',
      components: { "child-component": ChildComponent},


    methods: {
        updateTitleText(title)
        {
           this.title = title
    }
  }
</script>
