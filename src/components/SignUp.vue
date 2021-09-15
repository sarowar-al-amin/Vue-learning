<!--- Checking form validation -->
<template>
  <div>
     <p v-if="error.length">
      <b>Please correct the following errors</b>
      <ul>
        <li v-for="e in error" :key="e.id"> {{e}} </li>
      </ul>
     </p>
    <form @submit="signUp">
      <input type="text" placeholder="Enter your name" v-model="name"><br> <br>
      <input type="password" placeholder="Enter yout password" v-model="password"><br> <br>
      <button type="submit">SignUp</button>
    </form>
  </div>
</template>

<script>
export default{
  name: 'SignUp',
  data(){
    return{
        error: [],
        name: null,
        password: null
    }
  },
  methods: {
    signUp(e){
      if(this.name && this.password){
        console.log(`SignUp successfully`)
      }
      this.error=[]
      if(!this.name){
        this.error.push(`Name is required`)
      }
      if(!this.password){
        this.error.push(`Password is required`)
      }
      // console.warn(this.error)
      e.preventDefault()
    }
  }
}
</script>

<style scoped> 

</style>