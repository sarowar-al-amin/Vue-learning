<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{ title }}</h1>
    <HelloWorld msg="Learning Vue Js" v-on:titleChange="updateTitle($event)"/>
    <second v-bind:users='users'/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import second from './components/Second.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    second
  },
  data(){
    return {
      title: `Somebodies gonna lean on me`,
      users: [
        {name: 'sajib', email: 'sajib@sajib.com'},
        {name: 'rajib', email: 'rajib@sajib.com'},
        {name: 'mujib', email: 'mujib@sajib.com'},
      ]
    }
  },
  methods:{
    updateTitle(title){
      this.title = title
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
