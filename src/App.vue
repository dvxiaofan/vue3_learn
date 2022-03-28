<script setup>

import { ref } from 'vue';

const message = ref('HELLO CCYOU');

function reverseMessage() {
  message.value = message.value.split('').reverse().join('');
}

function notify() {
  alert('Navigation was prevented');
}

</script>

<template>
  <h1>{{ message }}</h1>

  <button @click="reverseMessage">翻转字符串</button>

  <button @click="message += '!'">添加！</button>

  <a href="https://github.com" @click.prevent="notify">Go</a>
</template>

<style>
button, a {
  display: block;
  margin-bottom: 1em;
}
</style>