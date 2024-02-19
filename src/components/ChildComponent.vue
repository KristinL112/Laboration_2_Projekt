<template>
  <div>
    <p>{{ title }}</p>
    <button class="btn btn-primary mt-2" v-on:click="updateTitle">
      Chat with us
    </button>
  </div>
</template>

<script>
  export default {
    name: 'ChildComponent',
    props: ['title'],
    methods: {
      updateTitle() {
        this.$emit('changeTitle', 'Props has been passed')
      }
    }
  }
</script>

<style scoped>
  button {
    display: flex;
  }
</style>
