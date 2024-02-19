<template>
  <div class="app" :class="mode">
    <header>
      <NavBar v-bind:mode="mode" @toggle="toggle" />
      <!-- Nav -->
      <!-- <NavBar /> -->
      <!-- Footer -->
      <FooterComponent v-bind:mode="mode" @toggle="toggle" />
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
        mode: 'light'
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
    background-color: rgb(190, 212, 212);
    color: black;
  }

  .dark {
    background-color: #192734;
    color: #f3f3f3;
  }
</style>
