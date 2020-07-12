<!--
 * @Author       : cuixinyuan@xdf.cn
 * @Date         : 2020-07-12 17:45:32
 * @LastEditors  : cuixinyuan@xdf.cn
 * @LastEditTime : 2020-07-12 20:37:17
 * @Description  : 描述信息
--> 
<template>
  <div class="layout-wrap">
    <siderbar></siderbar>
    <app-main></app-main>
  </div>
</template>
<script>
import Siderbar from '@/views/layout/components/Siderbar/index' 
import AppMain from '@/views/layout/components/AppMain' 
export default {
  name:'Layout',
  components:{
    Siderbar,AppMain
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
.layout-wrap {
  display: flex;
}
</style>