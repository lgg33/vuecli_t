<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'app',
  components: {
  },
  created() {
    axios.get('api/cms/page/list/1/5')
            .then(res => {
              console.log(res);
            }).catch(err => {
              console.log(err);
            })
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
