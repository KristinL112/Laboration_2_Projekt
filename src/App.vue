<template>
  <div class="app" :class="mode">
    <header>
      <!-- toggler-->
      <NavBar v-bind:mode="mode" @toggle="toggle" />
      <!-- Nav -->
      <!-- <NavBar /> -->
      <!-- Footer -->
      <EmailForm v-bind:mode="mode" @toggle="toggle" />
      <FooterComponent v-bind:mode="mode" @toggle="toggle" />
    </header>
  </div>
</template>

<script setup>
  import NavBar from './components/NavBar.vue'
  import FooterComponent from './components/FooterComponent.vue'
</script>

<!-- if/else loop om det är dark eller light mode-->
<script>
  export default {
    name: 'app', // Namn på komponenten
    data() {
      return {
        mode: 'light'
      }
    },

    components: { NavBar, FooterComponent },

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
  /* Light mode*/
  .app {
    background-color: rgb(190, 212, 212);
    color: black;
  }
  /* Dark mode*/
  .dark {
    background-color: #1c252d;
  }
</style>
