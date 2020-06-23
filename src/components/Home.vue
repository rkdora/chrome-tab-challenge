<template>
  <div class="home">
    <h1>Let's Chrome Tab Challenge!!</h1>
    <button @click="start()">Start</button>
  </div>
</template>

<script>
export default {
  name: 'home',
  methods: {
    start() {
      for (let i = 0; i < 100; i++) {
        if (window.open('https://www.yahoo.co.jp/')) {
          console.log('No.' + i + ' success!');
        } else {
          console.log('No.' + i + ' blocked.');
        }
      }
    }
  }
}
</script>

<style scoped>
</style>
