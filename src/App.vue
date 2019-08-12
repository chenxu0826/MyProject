<template>
  <div id="app">
    <!--头部-->
    <navMenu></navMenu>
    <navHeader></navHeader>
    <router-view/>
    <navFooter></navFooter>
  </div>
</template>

<script>
import navHeader from './components/navHeader.vue' // 引入组件头部导航
import navMenu from './components/navMenu.vue' // 引入组件侧边栏导航
import navFooter from './components/navFooter.vue' // 引入组件底部导航
export default {
  name: 'App',
  components: {
    navHeader: navHeader, // 引入组件头部导航
    navMenu: navMenu, // 引入组件侧边栏导航
    navFooter: navFooter, // 引入组件底部导航
  },
}
</script>

<style>
body{
  margin:0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
