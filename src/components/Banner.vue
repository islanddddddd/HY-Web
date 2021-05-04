<template>
  <div id="banner">
    <el-carousel>
      <el-carousel-item v-for="item in imgList" :key="item">
        <el-image
            style="height: 100%"
            :src="item"
            fit="cover">
        </el-image>
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  name: "Banner",
  data: function () {
    return {
      imgList: [
        "https://w.wallhaven.cc/full/z8/wallhaven-z8mq8y.jpg",
        "https://w.wallhaven.cc/full/rd/wallhaven-rddgwm.jpg",
        "https://w.wallhaven.cc/full/pk/wallhaven-pk8pzj.png",
        // "https://w.wallhaven.cc/full/6q/wallhaven-6qlv6q.jpg",
      ]
    };
  },
  methods: {}
}
</script>

<style scoped>
#banner{
  /*margin: 0 15vw 0 15vw;*/
  /*z-index: -1;*/
}
.el-carousel {
  height: 30vw;
}

.el-carousel__item {
  height: 30vw;
}
</style>
