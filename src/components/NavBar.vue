<!--import av paket och komponenter, funktioner, vue methods -->
<script setup>
  import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <!--template är "html-filen" -->
  <header>
    <nav class="navbar navbar-expand-lg">
      <!--En PROPS-toggler, visar värdet "mode",rendera en ToggleComponent-->
      <div>{{ mode }}</div>
      <!--När ToggleComponent används sker händelsen "toggle" och uppdaterar parentkomponenten.-->
      <div><ToggleComponent :mode="mode" @toggle="$emit('toggle')" /></div>
      <!--toggler slut-->

      <!--Nav links-->
      <div class="container-fluid">
        <div id="wrapper-logo">
          <img src="../assets/img/university_logo_new.png" alt="logo" />
        </div>

        <RouterLink class="nav-link" to="/">
          <div class="sitename">Global University Guide</div>
        </RouterLink>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="offcanvas"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Offcanvas-meny som visasvid knapptryckning -->
        <div
          class="offcanvas offcanvas-end"
          tabindex="-1"
          id="navbarNav"
          aria-labelledby="navbarOffcanvasLgLabel"
        >
          <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="navbarOffcanvasLgLabel">
              Global University Guide
            </h5>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="offcanvas"
              aria-label="Close"
            ></button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
              <li class="nav-item">
                <RouterLink class="nav-link" to="/">Home</RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink class="nav-link" to="/about">About</RouterLink>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </header>
  <!-- RouterView används för att visa komponenten -->
  <RouterView />
</template>

<script>
  /* importerar Togglekomponenten */
  import ToggleComponent from '@/components/ToggleComponent.vue'
</script>

<style>
  header {
    line-height: 1.5;
    max-height: 100vh;
    transition: background-color 0, 3s ease-in-out;
  }

  #wrapper-logo img {
    margin: 0 auto; /* Bilden horisontellt */
    height: 60px; /* Gör bilden responsiv*/
  }

  .sitename {
    font-size: 2.5vh;
    color: black;
    background-color: rgb(190, 212, 212);

    padding-left: 1vh;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande',
      'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  }

  /* Stil för offcanvas-titeln, sätter textfärg till svart */
  .offcanvas-header {
    color: black;
  }

  /* Stil för navbar-toggler, sätter bakgrundsfärg till vit */
  .navbar-toggler {
    background-color: rgb(255, 255, 255);
  }

  .navbar {
    background-color: rgb(190, 212, 212);
    height: 12vh;
  }

  .nav-link:hover {
    background-color: azure;
  }

  /* Adjusting hamburger nav for mobile view */
  button.navbar-toggler {
    background-color: white;
    color: rgb(190, 212, 212);
  }

  /* DARK MODE nav */
  .dark header nav {
    background-color: #1c252d;
  }

  .dark header nav .nav-link {
    color: rgb(255, 255, 255);
  }

  .dark .sitename {
    background-color: #1c252d;
  }

  .dark header nav .nav-link:hover {
    color: #ffffff;
    background-color: #344555;
  }

  .dark header nav .sitename {
    color: rgb(255, 255, 255);
  }

  .dark button.navbar-toggler {
    background-color: white;
    color: #1c252d;
  }

  .dark .offcanvas {
    background-color: #344555;
  }
  /* DARK MODE nav END*/
</style>
