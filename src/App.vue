<template>
  <h3> {{ message }} </h3>
  <h5> {{ length }} </h5>
  <button @click='handleClick'>Add (!) to message</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      message: 'Hello, Vue from Stackpython!'
    };
  },
  computed: {
    length() {
      return this.message.length;
    }
  },
  methods: {
    handleClick() {
      this.message = this.message + '!';
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
