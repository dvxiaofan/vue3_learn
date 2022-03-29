<script>

export default {
  data() {
    return {
      message: 'Options message',
      isRed: true,
      color: 'blue',
    }
  },

  methods: {
    toggleRed() {
      this.isRed = !this.isRed
    },

    toggleColor() {
      this.color = this.color === 'blue' ? 'green' : 'blue'
    },
  },

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