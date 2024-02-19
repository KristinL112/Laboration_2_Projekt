<template>
  <div class="card-group">
    <div class="card">
      <img
        src="../assets/img/library.jpg"
        class="card-img-top"
        alt="Univeristy"
      />
      <div class="card-body">
        <h5 class="card-title">Highest-ranked universities</h5>
        <p class="card-text">
          This is a longer card with supporting text below as a natural lead-in
          to additional content. This content is a little bit longer.This is a
          longer card with supporting text below as a natural lead-in to
          additional content. This content is a little bit longer.
        </p>
        <button
          class="btn btn-primary"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#collapseExample"
          aria-expanded="false"
          aria-controls="collapseExample"
        >
          Read more
        </button>

        <div class="collapse" id="collapseExample">
          <div class="card card-body">
            Some placeholder content for the collapse component. This panel is
            hidden by default but revealed when the user activates the relevant
            trigger.
          </div>
        </div>
      </div>
    </div>
    <div class="card">
      <img
        src="../assets/img/students.jpg"
        class="card-img-top"
        alt="Students"
      />
      <div class="card-body">
        <h5 class="card-title">Research integrity and ethics</h5>
        <p class="card-text">
          This is a wider card with supporting text below as a natural lead-in
          to additional content. This card has even longer content than the
          first to show that equal height action.
        </p>
      </div>
    </div>
    <div class="card">
      <img
        src="../assets/img/laptop.jpg"
        class="card-img-top"
        alt="Woman with laptop"
      />
      <div class="card-body">
        <h5 class="card-title">Research integrity and ethics</h5>
        <p class="card-text">
          This is a wider card with supporting text below as a natural lead-in
          to additional content. This card has even longer content than the
          first to show that equal height action.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .card-body {
    margin: 0 auto; /* Bilden horisontellt */
    height: auto; /* Gör bilden responsiv */
    overflow-x: hidden; /* Döljer horisontell overflow av bilden */
    padding-bottom: 2vh;
  }
</style>
