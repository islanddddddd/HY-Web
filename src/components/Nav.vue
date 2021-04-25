<template>

  <div>
    <el-row>
      <el-col :span="24">
        <div class="grid-content ">
          <div id="c" :style="{background:'url('+imgurl+')',backgroundSize: '100% auto'}"></div>
          <el-carousel :interval="0" type="card" indicator-position="none" @change="change">
            <el-carousel-item v-for="item in imglist" :key="item"
                              :style="{background:'url('+item+')',backgroundSize: '100% auto'}">
            </el-carousel-item>
          </el-carousel>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data: function () {
    return {
      imglist: [
        "https://w.wallhaven.cc/full/z8/wallhaven-z8mq8y.jpg",
        "https://w.wallhaven.cc/full/rd/wallhaven-rddgwm.jpg",
        "https://w.wallhaven.cc/full/pk/wallhaven-pk8pzj.png",
        "https://w.wallhaven.cc/full/6q/wallhaven-6qlv6q.jpg",
      ],
      imgurl: "https://w.wallhaven.cc/full/z8/wallhaven-z8mq8y.jpg",
      nrp: "no-repeat"
    };
  },
  methods: {
    change: function (item) {
      this.imgurl = this.imglist[item]
    }
  }
}
</script>

<style scoped>
#c {
  position: absolute;
  /*z-index: -1;*/
  background: url("../assets/logo.png");
  width: 100%;
  height: 100%;
  margin: -20vh;
  filter: blur(5px);
}

.el-row {
  margin-bottom: 20px;

}

:last-child {
  margin-bottom: 0;
}

.el-col {
  border-radius: 4px;
}

.bg-purple-dark {
  background: #99a9bf;
}

.bg-purple {
  background: #d3dce6;
}

.bg-purple-light {
  background: #e5e9f2;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
  padding: 20vh;
}

.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
<style scoped>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #E4E7ED;

}

.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;

}
</style>