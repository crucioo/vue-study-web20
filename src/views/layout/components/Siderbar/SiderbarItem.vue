<!--
 * @Author       : cuixinyuan@xdf.cn
 * @Date         : 2020-07-12 17:57:34
 * @LastEditors  : cuixinyuan@xdf.cn
 * @LastEditTime : 2020-07-12 21:25:21
 * @Description  : 描述信息
--> 
<template>
  <div>
    <template v-if="!routeItem.children">
      <!-- <router-link :to="routeItem.path"> -->
        <el-menu-item :index="routeItem.path">{{routeItem.name}}</el-menu-item>
      <!-- </router-link> -->
    </template>
    
    

    <el-submenu v-else :index="routeItem.path">
      <template slot="title">
        <i class="el-icon-location"></i>
        <span slot="title">{{routeItem.name}}</span>
      </template>
      <siderbar-item 
        v-for="child in routeItem.children"
        :key="child.path"
        :routeItem="child"
      />
    </el-submenu>

  </div>
</template>
<script>
export default {
  name:'SiderbarItem',
  props: {
    routeItem:{
      type:Object
    }
  },
  data() {
    return {

    };
  },
  created() {},
  methods: {

  },
}
</script>
<style scoped>
</style>`