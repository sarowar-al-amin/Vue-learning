<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="alertMe">Alert function calling</button>
    <h3>{{ data }}</h3>
    <button @click="loveSong('Selena Gomez')">Singer</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    alertMe(){
      alert(`You remember me --- James Moriatee`);
    },
    loveSong(item){
      console.log(`love you like a love song baby -- ${item}`);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
