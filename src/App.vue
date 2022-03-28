<script>

export default {
  data() {
    return {
      message: 'HELLO XIAOFAN',
    }
  },

  methods: {
    reverseMessage() {
      this.message = this.message.split('').reverse().join('')
    },

    notify() {
      alert('lslkajfl;kajs;fkj;fkjsa;flk')
    },

  },
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