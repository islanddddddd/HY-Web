<template>
  <div id="app">
    <Banner></Banner>
  </div>
</template>

<script>

import Banner from "@/components/Banner";

export default {
  name: 'app',
  components: {
    Banner
  }
}
</script>

<style>
body{
  margin: 0px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>
