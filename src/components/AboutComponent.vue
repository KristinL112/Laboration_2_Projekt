<template>
  <div>
    <!-- <p>{{ message }}</p> -->
  </div>
  <div class="about-card">
    <div class="row row-cols-1 row-cols-md-2 g-4">
      <div class="col">
        <div class="card">
          <img
            src="../assets/img/library.jpg"
            class="card-img-top"
            alt="Univeristy"
          />
          <div class="card-body">
            <h5 class="card-title">Highest-ranked universities</h5>
            <p class="card-text">
              This is a longer card with supporting text below as a natural
              lead-in to additional content. This content is a little bit
              longer.
            </p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <img
            src="../assets/img/friends.jpg"
            class="card-img-top"
            alt="People"
          />
          <div class="card-body">
            <h5 class="card-title">Research integrity and ethics</h5>
            <p class="card-text">
              This is a longer card with supporting text below as a natural
              lead-in to additional content. This content is a little bit
              longer.
            </p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <img
            src="../assets/img/students.jpg"
            class="card-img-top"
            alt="Students"
          />
          <div class="card-body">
            <h5 class="card-title">Collaboration partnership</h5>
            <p class="card-text">
              This is a longer card with supporting text below as a natural
              lead-in to additional content. This content is a little bit
              longer.
            </p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <img
            src="../assets/img/laptop.jpg"
            class="card-img-top"
            alt="Woman with laptop"
          />
          <div class="card-body">
            <h5 class="card-title">Facts in numbers</h5>
            <p class="card-text">
              This is a longer card with supporting text below as a natural
              lead-in to additional content. This content is a little bit
              longer.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .about-card {
    margin: 0 auto; /* Bilden horisontellt */
    height: auto; /* Gör bilden responsiv */
    overflow-x: hidden; /* Döljer horisontell overflow av bilden */
    padding-bottom: 2vh;
  }
</style>
