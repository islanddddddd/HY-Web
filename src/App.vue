<template>
  <div id="app">
    <Nav></Nav>
    <Banner></Banner>
    <div id="home_content">
      <el-row :gutter="20">
        <el-col :span="16">
          <div id="home_news">
            <News></News>
          </div>
        </el-col>
        <el-col :span="8">
          <div id="home_other">
            <Twitter></Twitter>
          </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>

import Banner from "@/components/Banner";
import News from "@/components/News";
import Twitter from "@/components/Twitter";
import Nav from "@/components/Nav";

export default {
  name: 'app',
  components: {
    Nav,
    Twitter,
    News,
    Banner
  }
}
</script>

<style>
#home_other {
  /*height: 50vh;*/
  /*background-color: deepskyblue;*/
}

#home_news {
  /*height: 50vh;*/
  /*background-color: #2c3e50;*/
}

#home_content {
  width: 70vw;
  height: 50vh;
  margin: 5vh 15vw 0 15vw;
  /*background-color: #42b983;*/
}

body {
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
