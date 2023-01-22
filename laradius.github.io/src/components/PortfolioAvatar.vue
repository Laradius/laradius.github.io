<template>
  <div class="headline">
    <h3 class="text-h3">Welcome to portfolio of</h3>
    <h1 class="text-h1">Elliot White</h1>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.headline {
  margin: 2rem 0;
}

h1 {
  font-family: verve;
  position: relative;
  padding: 0 2rem;
}

h3 {
  font-family: calluna;
  position: relative;

  padding: 0 2rem;

  &::before {
    position: absolute;
    content: '';
    height: 5px;
    width: 50%;
    top: 50%;
    left: 0;
    transform: translate(-100%, -50%);
    border: 0;
    border-top: 5px solid $hr-color;
  }

  &::after {
    position: absolute;
    content: '';
    height: 5px;
    width: 50%;
    top: 50%;
    right: 0;
    transform: translate(100%, -50%);
    border: 0;
    border-top: 5px solid $hr-color;
  }
}
</style>
