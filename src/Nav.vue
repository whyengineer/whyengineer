<template>
  <div>
        <el-menu
        :default-active="activeIndex2"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect">
            <el-menu-item index="1"><img src="https://img.whyengineer.com/logo.png?imageView2/1/w/46/h/46/q/75|imageslim"><span style="font-size:18px"> WhyEngineer</span></el-menu-item>
            <el-submenu index="2">
                <template slot="title">硬件</template>
                <el-menu-item index="2-1" disabled>ESP32-Cricle</el-menu-item>
                <el-menu-item index="2-2" disabled>ESP32-Snow</el-menu-item>
                <el-menu-item index="2-3">ESP32-Lin</el-menu-item>
            </el-submenu>
            <el-menu-item index="3">软件</el-menu-item>
            <el-menu-item index="4">维基</el-menu-item>
            <el-menu-item index="5">Github</el-menu-item>
        </el-menu>
  </div>
</template>



<script>
  export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>