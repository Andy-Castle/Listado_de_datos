<template>
  <div>
    <RouterLink v-for="item in menuItemsFiltered" :key="item.id" :to="item.path">
      {{ item.title }}
    </RouterLink>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
import type { IMenu } from '@/interfaces/IMenu'

const props = defineProps<{
  menuItems: IMenu[]
}>()

const menuItemsFiltered = props.menuItems.filter((item, index) => index % 2 === 0)
</script>
