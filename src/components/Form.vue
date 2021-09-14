<template>
  <div>
    <input type='text' v-model="lorginForm.userName" placeholder='Enter your name'><br><br>
    <input type='password' v-model="lorginForm.password" placeholder='Enter your password'><br><br>
    <button @click="login">Login</button>
  </div>
</template>

<script>
  export default{
    name:'Form',
    data(){
      return{
        lorginForm:{
          userName: null,
          password: null
        }
      }
    },
    methods:{
      login(){
        console.log(this.lorginForm.userName + ' ' + this.lorginForm.password)
      }
    }
  }
</script>

<style scoped>

</style>