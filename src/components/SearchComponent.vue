<template>
  <section class="hero">
    <h2 id="title" class="text-center mt-5">Search university</h2>
    <div class="container text-center">
      <div class="row">
        <div class="col-12">
          <input
            v-model="countryName"
            id="search-input"
            class="form-control"
            placeholder="Search for a university or country"
          />

          <!-- En knapp för att söka -->

          <div class="button">
            <a
              type="button"
              href="#"
              v-on:click.prevent="fetchData"
              class="btn btn-primary mt-2"
              >Search</a
            >
          </div>

          <div v-for="country in countries" :key="country.name">
            <ul class="list-group">
              <li class="list-group-item">
                <h4>{{ country.name }}</h4>
              </li>
              <li class="list-group-item">
                <p>{{ country.country }}</p>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        countries: [],
        countryName: ''
      }
    },
    methods: {
      async fetchData() {
        if (this.countryName.length == 0) {
          return
        }
        try {
          const response = await fetch(
            `http://universities.hipolabs.com/search?country=${this.countryName}`
          )
          const result = await response.json()

          this.countries = result
        } catch (error) {
          console.log('An error occurred:', error)
        }
      }
    }
  }
</script>

<style>
  .btn {
    background-color: rgb(190, 212, 212);
    color: black;
    border: none;
    border-radius: 12px;
  }
  .btn:hover {
    background-color: rgb(87, 147, 155);
  }

  .hero {
    margin-bottom: 1vh;
  }
</style>
