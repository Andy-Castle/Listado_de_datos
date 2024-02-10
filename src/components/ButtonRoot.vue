<template>
  <div>
    <button @click="GoToRoot">Ir a la raíz</button>
  </div>
</template>

<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()

const GoToRoot = () => {
  router.push('/')
}
</script>
