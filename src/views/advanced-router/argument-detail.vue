<template>
  <div>
    <basic-container>
      <el-tag>菜单中还是父类高亮，参考mock/menu.js里的group配置</el-tag>
      <el-tag type="success">参数路由接受参数{{$route.query}}</el-tag>
    </basic-container>
    <basic-container>
      <el-button type="primary"
                 @click="breaks">关闭返回列表</el-button>
    </basic-container>
  </div>
</template>

<script>
export default {
  methods: {
    breaks () {
      this.$router.$avueRouter.closeTag();
      this.$router.push({ path: '/advanced-router/argument-page' })
    }
  }
};
</script>

<style>
</style>
