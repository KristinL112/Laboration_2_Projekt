<template>
  <div class="app" :class="mode">
    <NavBar v-bind:mode="mode" @toggle="toggle" />
    <header>
      <!-- Nav -->
      <!-- <NavBar /> -->
      <!-- Footer -->
      <FooterComponent />
    </header>
  </div>
</template>

<script setup>
  import NavBar from './components/NavBar.vue'
  import FooterComponent from './components/FooterComponent.vue'
</script>

<script>
  export default {
    name: 'app', // Namn på komponenten
    components: { navBar: NavBar },
    data() {
      return {
        mode: 'dark'
      }
    },
    methods: {
      toggle() {
        if (this.mode === 'dark') {
          this.mode = 'light'
        } else {
          this.mode = 'dark'
        }
      }
    }
  }
</script>

<style>
  .app {
    background-color: rgb(210, 218, 225);
    color: black;
  }

  .dark {
    background-color: #192734;
    color: #f3f3f3;
  }
</style>
