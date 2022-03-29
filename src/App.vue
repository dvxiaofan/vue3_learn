<script setup>
import { ref } from 'vue'
import HelloWorld from '@/components/HelloWorld.vue'

const todoList = ref([
  {id: 0, text: 'Vegetables'},
  {id: 1, text: 'Cheese'},
  {id: 2, text: 'Whatever else humans are supposed to eat'},
])
</script>

<template>
  <ol>
    <HelloWorld
        v-for="item in todoList"
        :todo="item"
        :key="item.id"
    ></HelloWorld>
  </ol>
</template>