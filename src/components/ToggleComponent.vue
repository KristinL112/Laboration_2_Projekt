<template>
  <div class="toggle-wrapper">
    <label class="toggle">
      <!-- I denna variabel kollas om mode är lika med dark  -->
      <input type="checkbox" :checked="mode === ''" @change="$emit('toggle')" />
      <span class="toggler round"></span>
    </label>
  </div>
</template>

<!-- Props  -->
<script>
  export default {
    props: ['mode']
  }
</script>

<style>
  .toggle {
    position: absolute;
    display: inline-block;
    position: center;
    width: 50px;
    height: 25px;

    top: 75%; /* Centrerar vertikalt */
    left: 50%; /* Centrerar horisontellt  */
    transform: translate(-50%, -50%);
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
  }

  .toggler:before {
    position: absolute;

    content: '';
    height: 18px;
    width: 18px;
    left: 4px;
    bottom: 4px;
    background-color: #fff;
    -webkit-transition: 0.4s;
    transition: 0.4s;
  }
  /* Tar input till toggler */
  input:checked + .toggler {
    background-color: #415669;
  }

  input:focus + .toggler {
    box-shadow: 0 0 2px #415669;
  }

  /* Toggler är checked och unchecked */
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
