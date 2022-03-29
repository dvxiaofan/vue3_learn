<script setup>
import { ref } from 'vue'

const message = ref('This is title message')
const isRed = ref(true)
const color = ref('green')

function toggleRed() {
  isRed.value = !isRed.value
}

function toggleColor() {
  color.value = color.value === 'green' ? 'blue' : 'green'
}

</script>

<template>
  <p>
    <span :title="message">
      Hover me to show my title
    </span>
  </p>

  <p :class="{red: isRed}" @click="toggleRed">
    This red color? Click me
  </p>

  <p :style="{color}" @click="toggleColor">
    What color me now? Click to toggle
  </p>

</template>

<style>
button, a {
  display: block;
  margin-bottom: 1em;
}

.red {
  color: red
}
</style>