<template>
  <Greeting nombre ="Rodrigo1"  />
</template>

<script setup>
  import {ref} from 'vue'
  import Greeting from './components/Greeting.vue';

  //const nombre = ref('Rodrigo')
  //const fecha = new Date().toLocaleDateString()
</script>

<style>
  .app {
    text-align: center;
    font-family: Arial, sans-serif;
    margin-top: 100px;
  }
</style>


