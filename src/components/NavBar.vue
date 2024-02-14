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
        <RouterLink class="navbar-brand" to="/">UNIVERSITY</RouterLink>
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
            <!-- <li class="nav-item">
              <RouterLink class="nav-link" aria-current="page" to="/"
                >Lorem ipsum</RouterLink
              >
            </li> -->
            <li class="nav-item">
              <RouterLink class="nav-link" to="/">Home</RouterLink>
            </li>

            <li class="nav-item">
              <RouterLink class="nav-link" to="/about"
                >University facts</RouterLink
              >
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
  /* Changeing backround color */

  .navbar {
    background-color: rgb(169, 203, 203);
    height: 10vh;
  }

  #navbarNav {
    justify-content: flex-end;
  }
  .sitename {
    position: absolute; /* Absolut positionering relativt till första föräldern med relativ eller absolut positionering */
    top: 50%; /* Centrerar vertikalt till 50% av förälderns höjd */
    left: 50%; /* Centrerar horisontellt till 50% av förälderns bredd */
    transform: translate(
      -50%,
      -50%
    ); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */
  }
  /* Adjusting hamburger nav for mobile view */
  button.navbar-toggler {
    background-color: white;
    color: white;
  }
</style>
