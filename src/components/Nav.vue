<template>
  <div id="nav">
    <el-affix>
      <el-menu class="el-menu-demo" mode="horizontal" text-color="#919398" active-text-color="#919398">
        <el-row type="flex" class="row-bg" justify="space-around">
          <el-col :span="6">
            <el-menu-item index="1">
              <i>Title</i>
            </el-menu-item>
          </el-col>
          <el-col :span="4">
            <el-menu-item index="1">
              <i class="el-icon-news"> NEWS</i>
            </el-menu-item>
          </el-col>
          <el-col :span="4">
            <el-menu-item index="1">
              <i class="el-icon-s-platform"> 新作情报</i>
            </el-menu-item>
          </el-col>
          <el-col :span="4">
            <div>
              <el-menu-item index="1">
                <i class="el-icon-chat-round"> Blog</i>
              </el-menu-item>
            </div>
          </el-col>
          <el-col :span="6">
            <el-menu-item index="1">
              其他链接
            </el-menu-item>
          </el-col>
        </el-row>
      </el-menu>
    </el-affix>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {};
  },
  methods: {}
}
</script>

<style scoped>
.el-menu-item [class^=el-icon-] {
  font-size: 24px;
}

i {
  font-size: 24px;

}

#nav {
  /*font-size: 50px;*/
  /*height: 10vh;*/
  /*position: ;*/
  /*z-index: 1000;*/
  /*opacity: 1;*/
}
</style>