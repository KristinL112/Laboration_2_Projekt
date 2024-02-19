<template>
  <div class="toggle-wrapper">
    <label class="toggle">
      <input
        type="checkbox"
        :checked="mode === 'dark'"
        @change="$emit('toggle')"
      />

      <span class="toggler round"></span>
    </label>
  </div>
</template>

<script>
  export default {
    props: ['mode']
  }
</script>

<style>
  .toggle {
    position: absolute;
    display: inline-block;
    width: 47px;
    height: 24px;

    top: 70%; /* Centrerar vertikalt */
    left: 50%; /* Centrerar horisontellt  */
  }

  .toggle input {
    opacity: 0;
    width: 0;
    height: 0;
  }

  .toggler {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #32404e;
    -webkit-transition: 0.4s;
    transition: 0.4s;
  }

  .toggler:before {
    position: absolute;
    content: '';
    height: 18px;
    width: 18px;
    left: 1px;
    bottom: 3px;
    background-color: #fff;
    -webkit-transition: 0.4s;
    transition: 0.4s;
  }

  input:checked + .toggler {
    background-color: #415669;
  }

  input:focus + .toggler {
    box-shadow: 0 0 2px #415669;
  }

  input:checked + .toggler:before {
    -webkit-transform: translateX(26px);
    -ms-transform: translateX(26px);
    transform: translateX(26px);
  }

  .toggler.round {
    border-radius: 34px;
  }

  .toggler.round:before {
    border-radius: 50%;
  }
</style>
