<script>
export default {
  data() {
    return {
      isShow: false,
      list: [1, 2, 3, 4, 5],
    }
  },
}
</script>

<template>
  <button @click="isShow = !isShow">Toggle show list</button>
  <button @click="list.push(list.length+1)">Push Number</button>
  <button @click="list.pop()">Pop Number</button>
  <button @click="list.reverse()">Reverse Number</button>

  <ul v-if="isShow && list.length">
    <li v-for="item of list">{{ item }}</li>
  </ul>

  <p v-else-if="list.length">List is not empty, but had hidden</p>
  <p v-else>List is Empty</p>

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