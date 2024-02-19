<template>
  <button class="btn" :style="{ backgroundColor: bgColor }">{{ name }}</button>
</template>
<script>
  export default {
    props: {
      name: String,
      bgColor: String
    }
  }
</script>
