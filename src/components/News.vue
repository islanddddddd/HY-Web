<template>
  <div class="block">
    <el-timeline>
      <el-timeline-item v-for="item in newsList" :key="item" :timestamp=item.time placement="top" size="large">
        <el-card>
          <el-row :gutter="100">
            <el-col :span="4">
              <el-image
                  style="width: 100px; height: 100px"
                  :src="item.imgUrl"
                  fit="cover">
              </el-image>
            </el-col>
            <el-col :span="20">
              <h4>{{ item.title }}</h4>
              <p>{{ item.content }}</p>
            </el-col>
          </el-row>
        </el-card>
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script>
export default {
  name: "News",
  data: function () {
    return {
      newsList: {
        "1": {
          "time": "2020/1/29",
          "title": "演示的标题",
          "content": "随便写的一大串内容，这串内容虽然说什么意义都没有，但它是最好的演示demo。",
          "imgUrl": "https://img1.baidu.com/it/u=1709216491,2536617744&fm=26&fmt=auto&gp=0.jpg"
        }, "2": {
          "time": "2020/1/29",
          "title": "演示的标题",
          "content": "随便写的一大串内容，这串内容虽然说什么意义都没有，但它是最好的演示demo。",
          "imgUrl": "https://img1.baidu.com/it/u=1709216491,2536617744&fm=26&fmt=auto&gp=0.jpg"
        }, "3": {
          "time": "2020/1/29",
          "title": "演示的标题",
          "content": "随便写的一大串内容，这串内容虽然说什么意义都没有，但它是最好的演示demo。",
          "imgUrl": "https://img1.baidu.com/it/u=1709216491,2536617744&fm=26&fmt=auto&gp=0.jpg"
        }, "4": {
          "time": "2020/1/29",
          "title": "演示的标题",
          "content": "随便写的一大串内容，这串内容虽然说什么意义都没有，但它是最好的演示demo。",
          "imgUrl": "https://img1.baidu.com/it/u=1709216491,2536617744&fm=26&fmt=auto&gp=0.jpg"
        },
      }
    };
  },

}
</script>

<style scoped>
.el-timeline-item {
  text-align: left;
}
</style>