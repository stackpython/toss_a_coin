<template>
  <h3>status: {{ status }}</h3>
  <button @click='toss'>Toss</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      status: 'H'
    }
  },
  methods: {
    toss() {
      const hOrT = 'HT';
      this.status = hOrT[Math.floor(Math.random() * 2)];
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
