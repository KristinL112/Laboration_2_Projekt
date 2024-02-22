<script></script>
<!-- En hero-bild med fluid class för responsivitet-->
<template>
  <main>
    <div id="wrapper-hero">
      <img
        src="../assets/img/people-6027028_1920_2.jpg"
        class="img-fluid"
        alt="students"
      />
      <!--Centrering av text -->
      <div class="centered">
        <!-- Rubrik-->
        <h1>Find your dream university today</h1>
      </div>
    </div>
  </main>
</template>

<style>
  #wrapper-hero img {
    margin: 0 auto; /* Bilden horisontellt */
    height: auto; /* Gör bilden responsiv*/
    overflow-x: hidden; /* Döljer horisontell overflow av bilden */
  }

  /* Stilar för centrerad text */
  #wrapper-hero .centered {
    position: absolute;
    top: 30%; /* Centrerar vertikalt */
    left: 50%; /* Centrerar horisontellt  */
    transform: translate(
      -50%,
      -50%
    ); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */

    background-color: rgba(42, 62, 79, 0.8);
    padding: 1vh;
    color: white;

    border-radius: 3px;
  }
</style>
