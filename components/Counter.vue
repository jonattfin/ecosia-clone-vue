<template>
  <div class="counter">{{ counter.toLocaleString() }}</div>
</template>

<script>

export default {
  data() {
    return {
      counter: 146 * Math.pow(10, 6),
    }
  },
  mounted() {
    this.counterInterval = setInterval(() => {
      this.counter++
    }, 2000)
  },
  unmounted() {
    clearInterval(this.counterInterval)
  },
}
</script>

<style>
.counter {
  font-size: 2em;
  color: teal;
}
</style>
