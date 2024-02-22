<script setup>
  import EmailForm from '../components/EmailForm.vue'
</script>

<template>
  <EmailForm />

  <div class="card-footer text-body-secondary">
    <div>
      <RouterLink class="footer-link" to="/">Home</RouterLink>
    </div>
    <div>
      <RouterLink class="footer-link" to="/about">About</RouterLink>
    </div>
    <div class="footer-link">© 2024 Copyright: Kristin Lindén</div>
  </div>
</template>

<style>
  .card-text {
    padding-top: 2vh;
  }

  #mail {
    margin-top: 2vh;
  }
  .form-wrap {
    padding-top: 1vh;
  }
  .alert {
    background-color: rgb(190, 212, 212);
    padding-top: 2vh;
  }
  .alert h5 {
    margin-bottom: 0rem;
  }
  .form-group {
    padding-top: 2vh;
  }

  .card-footer {
    background-color: rgb(190, 212, 212);
    padding-top: 5vh;
    padding-bottom: 5vh;
    padding-left: 5vh;
    padding-right: 5vh;
  }

  .footer-link {
    display: flex;
    justify-content: center;
    text-decoration: none;
    color: #000000;
    list-style: none;
  }

  /* Styles for dark mode here */

  .dark .card-footer {
    background-color: #1c252d;
  }

  .dark .footer-link {
    color: white;
  }
</style>
