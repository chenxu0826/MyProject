<template>
  <div class="nav-menu">
    <el-row class="tac">
      <el-col :span="24">
        <div class="menu-tit"><i class="el-icon-menu"></i>中台系统</div>
        <el-menu
          default-active="2"
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose"
          background-color="#545c64"
          text-color="#fff">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>设备配置</span>
            </template>
            <el-menu-item-group>
              <template slot="title">设备配置</template>
              <el-menu-item index="1-1">选项1</el-menu-item>
              <el-menu-item index="1-2">选项2</el-menu-item>
            </el-menu-item-group>
            <el-menu-item-group title="分组2">
              <el-menu-item index="1-3">选项3</el-menu-item>
            </el-menu-item-group>
            <el-submenu index="1-4">
              <template slot="title">选项4</template>
              <el-menu-item index="1-4-1">选项1</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span slot="title">设备状态监控</span>
          </el-menu-item>
          <el-menu-item index="3" disabled>
            <i class="el-icon-document"></i>
            <span slot="title">设备升级</span>
          </el-menu-item>
          <el-menu-item index="4">
            <i class="el-icon-setting"></i>
            <span slot="title">设备维护</span>
          </el-menu-item>
        </el-menu>
      </el-col>
    </el-row>
  </div>

</template>

<script>
  export default {
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>
<style lang="scss">
    .menu-tit{
      text-align: center;
      font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
      height: 10rem;
      line-height: 10rem;
      font-weight: bold;
      color: hsla(0,0%,100%,.65);
    }
    .nav-menu{
      flex: 0 0 256px;
      max-width: 256px;
      min-width: 256px;
      width: 256px;
      position: relative;
      z-index: 10;
      box-shadow: 2px 0 6px rgba(0,21,41,.35);
      float: left;
      min-height: 80vh;
      text-align: left;
      background: #001529;
    }
</style>
