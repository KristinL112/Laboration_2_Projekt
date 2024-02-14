<template>
  <section class="hero">
    <h1 id="title" class="text-center mt-5">Search university</h1>
    <div class="container text-center">
      <div class="row">
        <div class="col-12">
          <input
            v-model="countryName"
            type="text"
            id="search-input"
            class="form-control"
            placeholder="Search for a university or country"
          />
          <button @click="fetchData" class="btn btn-primary mt-2">
            Search
          </button>
          <div v-for="country in countries" :key="country.name">
            <div class="mb-3">
              <h4>{{ country.name }}</h4>
              <p>{{ country.country }}</p>
            </div>
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
        // Byt ut med det önskade landet
        const response = await fetch(
          `http://universities.hipolabs.com/search?country=${this.countryName}`
        )
        const result = await response.json()
        this.countries = result
      }
    }
  }
</script>

<style scoped>
  .btn {
    background-color: rgb(91, 165, 175);
    border: none;
    border-radius: 12px;
  }

  .hero {
    margin-bottom: 1vh;
  }
</style>
