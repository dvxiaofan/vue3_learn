<script setup>
import DemoGrid from '@/components/Grid.vue'
import { ref } from 'vue'

const searchQuery = ref('')
const gridColumns = ['name', 'power']
const gridData = [
  {name: 'CC You', power: Infinity},
  {name: 'XF fan', power: 9000},
  {name: 'dd kao', power: 7000},
  {name: 'rr you', power: 8000},
]
</script>

<template>
  <form id="search">
    Search <input name="query" v-model="searchQuery">
  </form>

  <DemoGrid :data="gridData" :columns="gridColumns"
            :filter-key="searchQuery"></DemoGrid>
</template>