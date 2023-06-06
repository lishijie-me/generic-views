<template>
  <div>
    <table>
      <tr>
        <td>编号</td>
        <td>用戶名</td>
        <td>電話</td>
        <td>地址</td>
      </tr>
      <tr v-for="(item,index) in tests">
        <td>{{index}}</td>
        <td>{{item.username}}</td>
        <td>{{item.phone}}</td>
        <td>{{item.address}}</td>
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


