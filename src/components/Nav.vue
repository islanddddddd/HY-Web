<template>
  <div id="nav">
    <el-menu id="mdNav" :default-active="activeIndex" @select="handleSelect" class="el-menu-demo" mode="horizontal"
             text-color="#919398">
      <el-row type="flex" class="row-bg" justify="space-around">

        <el-col :span="6">
          <el-menu-item>
            <i>Title</i>
          </el-menu-item>
        </el-col>

        <el-col :span="6" v-for="item in navItemList" :key="item">
          <el-menu-item>
            <i :class="item.i"> {{ item.title }}</i>
          </el-menu-item>
        </el-col>

      </el-row>
    </el-menu>

    <el-menu id="xsNav" :default-active="activeIndex" @select="handleSelect" class="el-menu-demo" mode="horizontal"
             text-color="#919398">
      <el-row type="flex" class="row-bg" justify="space-around">
        <el-col :span="20">
          <el-menu-item index="1">
            <i>Title</i>
          </el-menu-item>
        </el-col>
        <el-col :span="4">
          <el-menu-item index="2">
            <el-dropdown><span class="el-dropdown-link"><i class="el-icon-arrow-down el-icon--right"></i></span>
              <template #dropdown>
                <el-dropdown-menu v-for="item in navItemList" :key="item">
                  <el-dropdown-item>
                    <el-link :underline="false" :href="item.url">{{ item.title }}</el-link>
                  </el-dropdown-item>
                </el-dropdown-menu>
              </template>
            </el-dropdown>
          </el-menu-item>
        </el-col>
      </el-row>
    </el-menu>

  </div>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1',
      navItemList: {
        "1": {"title": "NEWS", "i": "el-icon-news", "url": ""},
        "2": {"title": "作品情报", "i": "el-icon-s-platform", "url": ""},
        "3": {"title": "BLOG", "i": "el-icon-chat-round", "url": ""},
      }
    };
  },
  methods: {
    // handleSelect(key, keyPath) {
    //   console.log(key, keyPath);
    // }
  }
}
</script>

<style scoped>
.el-menu-item [class^=el-icon-] {
  font-size: 24px;
}

@media (min-width: 600px) {
  #xsNav {
    display: none;
  }
}

@media (max-width: 600px) {
  #xsNav {
    display: inline;
  }

  #mdNav {
    display: none;
  }
}

.el-menu-item.is-active {
  color: #919398;
}

i {
  font-size: 24px;
}

#nav {
  /*font-size: 50px;*/
  /*height: 10vh;*/
  /*position: ;*/
  /*z-index: 1000;*/
  /*opacity: 0.5;*/
}
</style>