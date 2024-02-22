<template>
  <!--en class "app" och en class som binder till mode är dark eller light  -->
  <div class="app" :class="mode">
    <header>
      <!-- Nav -->
      <NavBar v-bind:mode="mode" @toggle="toggle" />
      <!-- Email -->

      <!-- Footer -->
      <FooterComponent v-bind:mode="mode" @toggle="toggle" />
    </header>
  </div>
</template>

<script setup>
  // Importerar Navbar och Footer
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

  /* Dark mode */
  .dark {
    background-color: #1c252d;
  }
</style>
