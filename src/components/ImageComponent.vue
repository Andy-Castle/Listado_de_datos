<template>
  <div>
    <button class="imageButton" @click="toggleImage">
      {{ mostrarImagen ? 'Ocultar Imagen' : 'Mostrar Imagen' }}
    </button>
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

.imageButton {
  padding: 10px 15px;
  background-color: #280274;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
}

.imageButton:hover {
  background-color: #3652ad;
}

.imageButton:active {
  background-color: #280274;
}
</style>
