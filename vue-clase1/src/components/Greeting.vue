<template>
  <div class="greeting">
    <h1>Hola {{ nombre }}</h1>
    <p>La fecha desde este mismo componente es: {{ fecha }}</p>
    <p>Contador: {{ contador }}</p>
    <button @click="incrementar">+ Sumar</button>
  </div>
</template>

<script setup>
  import {ref} from 'vue'

  const props = defineProps({
    nombre: String,
    })

  //variables de este mismo componente
  const fecha = new Date().toLocaleDateString()
  const contador = ref(0)

  function incrementar() {
    contador.value++
    
  }
</script>

<style scoped>
h1{
    color:black
}
  .greeting {
    text-align: center;
    font-family: Arial, sans-serif;
    margin-top: 10px;
    color:aqua
    
  }
</style>