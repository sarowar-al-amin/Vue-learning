<template>
  <div>
    <table border="2px">
      <tr>
        <td>Id</td>
        <td>Name </td>
        <td>Salary </td>
        <td>Age</td>
      </tr>
      <tr v-for="item in list" :key="item.id">
        <td>{{item.id}}</td>
        <td>{{item.employee_name}}</td>
        <td>{{item.employee_salary }}</td>
        <td>{{item.employee_age}}</td>
      </tr>
    </table>
  </div>
</template>

<script> 
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'

Vue.use(VueAxios, axios)
export default{
  name: 'DataFetchFromAPI',
  data(){
    return{
      list: undefined
    }
  },
  mounted(){
    Vue.axios.get("http://dummy.restapiexample.com/api/v1/employees")
    .then((resp) => {
      this.list = resp.data.data;
      // console.log(resp)
    })
  }
}
</script>

<style scoped>

</style>