<script setup lang="ts">
import { RouterLink } from 'vue-router'
import type { IMenu } from '@/interfaces/IMenu'

const props = defineProps<{
  menuItems: IMenu[]
}>()
</script>

<template>
  <div>
    <RouterLink
      v-for="(item, index) in menuItems"
      :key="item.id"
      :to="item.path"
      :class="{ 'no-ver': index % 2 !== 0 }"
    >
      {{ item.title }}
    </RouterLink>
  </div>
</template>

<style scoped>
.no-ver {
  pointer-events: none;
  opacity: 0.5;
}
</style>
