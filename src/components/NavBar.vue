<!--import av paket och komponenter, funktioner, vue methods -->
<script setup>
  import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <!--template är "html-filen" -->
  <header>
    <nav class="navbar navbar-expand-lg">
      <div class="container-fluid">
        <!-- En RouterLink som fungerar som en länk till startsidan -->
        <div>
          <RouterLink class="navbar-brand" to="/">
            <img
              src="../assets/img/logo.png"
              alt="Logo"
              width="50"
              height="50"
              class="d-inline-block align-text-top"
            />
            <span>UNIVERSITY</span>
          </RouterLink>
          <!-- En RouterLink som fungerar som en länk till startsidan -->

          <!-- <div class="logoname">
            <RouterLink class="navbar-brand" to="/">UNIVERSITY</RouterLink>
          </div> -->
        </div>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <RouterLink class="nav-link" to="/">Home</RouterLink>
            </li>
            <li class="nav-item">
              <RouterLink class="nav-link" to="/about">About</RouterLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
  <!-- RouterView används för att visa komponenten -->
  <RouterView />
</template>

<style scoped>
  span {
    font-size: 3vh;
  }
  .navbar {
    background-color: rgb(169, 203, 203);
    height: 10vh;
  }

  #navbarNav {
    justify-content: flex-end;
  }

  /* Adjusting hamburger nav for mobile view */
  button.navbar-toggler {
    background-color: white;
    color: white;
  }
</style>
