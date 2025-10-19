<template>
    <div class="form">
        <input v-model="nombre"
        type="text"
        placeholder="nombre">

        <input v-model.number="edad"
        type="number"
        placeholder="edad">

        <select v-model="selected">
            <option disabled value="">Seleccione un país</option>
            <option value="Chile">Chile</option>
            <option value="Argentina">Argentina</option>
            <option value="Perú">Perú</option>
        </select>

        <button @click="enviar">Enviar</button>

        <div v-if="show">
            <p>Nombre: {{nombre}}</p>
            <p>Edad: {{edad}}</p>
            <p>País: {{selected}}</p>
        </div>

        

    </div>
    

</template>
<script setup>
    import {ref} from 'vue'
    const nombre = ref('')
    const edad = ref(0)
    const selected = ref('')
    const show = ref(false)



    function enviar() {
        show.value = true
        console.log(nombre.value, edad.value, selected.value)
    }

</script>
<style scoped>
.form {
    text-align: center;
    font-family: Arial, sans-serif;
    margin-top: 10px;
    
    
  }
</style>