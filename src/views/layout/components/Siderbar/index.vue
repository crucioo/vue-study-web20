<!--
 * @Author       : cuixinyuan@xdf.cn
 * @Date         : 2020-07-12 17:58:20
 * @LastEditors  : cuixinyuan@xdf.cn
 * @LastEditTime : 2020-07-12 21:27:06
 * @Description  : 描述信息
--> 
<template>
  <div>
    <el-menu
      class="siderbar-menu"
      default-active="1-1"
    >
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span slot="title">一级菜单</span>
        </template>
        <el-menu-item index="1-1">二级菜单1</el-menu-item>
        <el-menu-item index="1-2">二级菜单2</el-menu-item>
        
        <el-submenu index="1-3">
          <template slot="title">
            <i class="el-icon-location"></i>
            <span slot="title">二级菜单3</span>
          </template>
          <el-menu-item index="1-3-1">三级菜单1</el-menu-item>
          <el-menu-item index="1-3-2">三级菜单2</el-menu-item>
          <el-menu-item index="1-3-3">三级菜单3</el-menu-item>
        </el-submenu>

      </el-submenu>

      <!-- <siderbar-item
        v-for="route in routes"
        :key="route.path"
        :routeItem="route"
      /> -->

    </el-menu>
  </div>
</template>
<script>
import SiderbarItem from './SiderbarItem'
export default {
  components:{
    SiderbarItem
  },
  props: {},
  data() {
    return {
      routes:[{
        path:'/first-1',
        name:'一级菜单1',
        children:[{
          path:'/second-1',
          name:'二级菜单1',
        },{
          path:'/second-2',
          name:'二级菜单2',
        },{
          path:'/second-3',
          name:'二级菜单3',
          children:[{
            path:'/third-1',
            name:'三级菜单1',
          }]
        }]
      }]
    };
  },
  created() {},
  methods: {

  }
}
</script>
<style scoped>
.siderbar-menu {
  width: 200px;
  min-height: 400px;
}

</style>