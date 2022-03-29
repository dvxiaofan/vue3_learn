<script setup>
import { ref } from 'vue'

const text = ref('old text')
const isChecked = ref(true)


</script>

<template>
  <h2>Input Text</h2>
  <input type="text" v-model="text">
  <br>
  <span>Input text is: {{text}}</span>

  <h2>Checkbox</h2>
  <input type="checkbox" v-model="isChecked">
  <br>
  <span>Checked: {{isChecked}}</span>



</template>