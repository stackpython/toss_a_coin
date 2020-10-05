<template>
  <h3>status: {{ status }}</h3>
  <button @click='toss'>Toss</button>
  <button @click='add'>Add Coin</button>
  <button @click='remove'>Remove Coin</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      status: ['H']
    }
  },
  methods: {
    toss() {
      const hOrT = 'HT';
      // this.status = hOrT[Math.floor(Math.random() * 2)];
      for (let i in this.status){
        this.status[i] = hOrT[Math.floor(Math.random() * 2)];
      }
    },
    add() {
      this.status.push('H');
    },
    remove() {
      this.status.pop();
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
