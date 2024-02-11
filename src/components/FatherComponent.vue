<template>
  <div>
    <ChildComponent :menuItems="menuItems" />
  </div>
</template>

<script setup lang="ts">
import ChildComponent from '@/components/ChildComponent.vue'
import MenuData from '@/data/MenuData'

const menuItems = MenuData
</script>
