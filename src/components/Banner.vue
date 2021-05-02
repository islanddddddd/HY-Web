<template>
  <div>
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
.el-carousel {
  height: 50vh;
}

.el-carousel__item {
  height: 50vh;
}
</style>
