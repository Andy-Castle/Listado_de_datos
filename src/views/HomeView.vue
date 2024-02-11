<script setup lang="ts">
import FatherComponent from '@/components/FatherComponent.vue'
</script>

<template>
  <main>
    <h1>Este es la raíz del sitio</h1>
    <h3>👇Esto es el FatherComponent</h3>
    <FatherComponent />
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 20px auto;
}

h1,
h3 {
  margin-bottom: 10px; /* Pequeña separación entre h1 y h3 */
}
</style>
