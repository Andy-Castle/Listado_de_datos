<template>
  <div>
    <button @click="toggleImage">{{ mostrarImagen ? 'Ocultar Imagen' : 'Mostrar Imagen' }}</button>
    <img v-if="mostrarImagen" src="/src/assets/images/Evan_You.jpg" alt="Evan You" />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const mostrarImagen = ref(false)

const toggleImage = () => {
  mostrarImagen.value = !mostrarImagen.value
}
</script>

<style scoped>
img {
  width: 400px;
}
</style>
