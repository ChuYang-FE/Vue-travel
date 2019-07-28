<template>
  <div id="app">
    <!-- 路由页面做缓存，除了Detail页面（即mouted钩子每次都会被执行）-->
    <keep-alive exclude="Detail">  
      <router-view/> <!-- 路由页面 -->
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>
