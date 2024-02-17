<template>
  <div>
    <button v-on:click="updateTitle">Update Title</button>
  </div>
</template>

<script>
  export default {
    name: 'ChildComponent',
    methods: {
      updateTitle() {
        this.$emit('changeTitle', 'Props has been passed')
      }
    }
  }
</script>
