<template>
  <h3> {{ message }} </h3>
  <h5> {{ length }} </h5>
</template>

<script>
// data เก็บข้อมูลที่ component นั้นๆ เก็บไว้
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
