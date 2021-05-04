<template>
  <div id="nav">
    <el-menu
        class="el-menu-demo"
        mode="horizontal">
      <el-row type="flex" class="row-bg" justify="space-around">
        <el-col :span="6">
          <div class="grid-content bg-purple">
            <el-menu-item index="1">Title</el-menu-item>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple-light">
            <el-menu-item index="1">几个导航条</el-menu-item>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple">
            <el-menu-item index="1">社交链接</el-menu-item>
          </div>
        </el-col>
      </el-row>
    </el-menu>
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
#nav {
  /*height: 10vh;*/
  /*position: ;*/
  opacity: 0.5;
}
</style>
<style scoped>
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
}

.row-bg {
  background-color: #f9fafc;
}
</style>