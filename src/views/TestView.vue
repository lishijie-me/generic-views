<template>
  <div>
    <table>
      <tr>
        <td>编号</td>
        <td>菜单名</td>
        <td>父节点</td>
        <td>请求编号</td>
      </tr>
      <tr v-for="(item,index) in tests">
        <td>{{index}}</td>
        <td>{{item.menuName}}</td>
        <td>{{item.parentId}}</td>
        <td>{{item.orderNum}}</td>
      </tr>
    </table>

  </div>
</template>

<script>
import axios from "axios"
export default {
  name: "TestView.vue",
  data(){
    return {
      tests:[]
    }
  },
  created() {
    const _this = this
    axios.get('http://localhost:9901/demo/test1').then(function (res){
      console.log(res.data)
      _this.tests = res.data
    })
  }
}
</script>

<style scoped>

</style>


