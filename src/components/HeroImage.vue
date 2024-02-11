<script></script>
<!-- En hero-bild med fluid class för responsivitet-->
<template>
  <div id="wrapper-hero">
    <img
      src="../assets/img/people-6027028_1920_2.jpg"
      class="img-fluid"
      alt="students"
    />
    <!--Centrering av text -->
    <div class="centered">
      <!-- Rubrik-->
      <h1>Find universities</h1>
    </div>
  </div>
</template>

<style>
  #wrapper-hero img {
    margin: 0 auto; /* Centrerar bilden horisontellt */
    height: auto; /* Gör bilden responsiv*/
    overflow-x: hidden; /* Döljer horisontell overflow av bilden */
  }

  /* Stilar för centrerad text */
  #wrapper-hero .centered {
    position: absolute; /* Absolut positionering relativt till första föräldern med relativ eller absolut positionering */
    top: 50%; /* Centrerar vertikalt till 50% av förälderns höjd */
    left: 50%; /* Centrerar horisontellt till 50% av förälderns bredd */
    transform: translate(
      -50%,
      -50%
    ); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */
    color: white; /* Sätter textfärg till vit */
  }
</style>
