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
          Quod iusto iste tempora harum laboriosam maxime rerum fuga natus?
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veniam
          aperiam vel accusantium laudantium illum aliquid explicabo voluptates
          debitis molestiae suscipit. Harum laboriosam maxime rerum fuga natus?
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Illum
          aliquid explicabo voluptates. Amet consectetur adipisicing elit.
        </p>
        <button
          class="btn btn-primary"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#collapseExample1"
          aria-expanded="false"
          aria-controls="collapseExample1"
        >
          Read more
        </button>

        <div class="collapse" id="collapseExample1">
          <div class="card card-body">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam vel
            voluptate soluta voluptatem commodi? Illo id repellat facere fuga
            vero laudantium, earum unde deleniti, consequatur eum. Impedit.
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
          first to show that equal height action. Lorem ipsum dolor sit amet
          consectetur adipisicing elit. Alias cum accusamus laudantium sapiente.
          Consequatur quis officiis aperiam molestias facilis perferendis nemo,
          cupiditate deserunt odio libero doloribus iusto quod, quas hic.
        </p>

        <button
          class="btn btn-primary"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#collapseExample2"
          aria-expanded="false"
          aria-controls="collapseExample2"
        >
          Read more
        </button>

        <div class="collapse" id="collapseExample2">
          <div class="card card-body">
            Illo id repellat facere fuga vero laudantium, earum unde deleniti,
            est dolorem facilis consequatur eum. Impedit.Lorem ipsum dolor sit
            amet consectetur adipisicing elit. Quam vel voluptate soluta
            voluptatem commodi?
          </div>
        </div>
      </div>
    </div>
    <div class="card">
      <img
        src="../assets/img/laptop.jpg"
        class="card-img-top"
        alt="Woman with laptop"
      />
      <div class="card-body">
        <h5 class="card-title">Facts in numbers</h5>
        <p class="card-text">
          Beatae natus illum, culpa exercitationem nulla soluta rem rerum.
          Beatae culpa ipsam nam quam tempora labore, aut non natus sequi
          doloremque placeat. Lorem ipsum dolor sit amet consectetur adipisicing
          elit. Unde nihil ea odit distinctio molestias! Ipsa, optio nam
          dignissimos excepturi aperiam nulla quod repudiandae ex facilis saepe
          tempore, libero ipsum iusto! Lorem ipsum dolor sit amet consectetur
          adipisicing elit.
        </p>
        <button
          class="btn btn-primary"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#collapseExample3"
          aria-expanded="false"
          aria-controls="collapseExample3"
        >
          Read more
        </button>

        <div class="collapse" id="collapseExample3">
          <div class="card card-body">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam vel
            voluptate soluta voluptatem commodi? Illo id repellat facere fuga
            vero laudantium, earum unde deleniti, est dolorem facilis
            consequatur eum. Impedit.
          </div>
        </div>
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
