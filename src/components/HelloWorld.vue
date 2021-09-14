<template>
  <div class="hello">
    <h1 v-if="isCondition">{{ msg }}</h1>
    <h1 v-else> Hard code </h1>
    <button @click="alertMe">Alert function calling</button>
    <!-- String interpolation -->
    <h3> {{ message }} </h3> 
    <button @click="changeHardCode">Change Hard code</button>

    <table border="2px">
      <tr>
        <td>ID </td><td> Name </td><td> Email</td>
      </tr>
      <tr v-for="user in users" :key="user.id">
        <td> {{ user.id }} </td><td> {{ user.name }} </td><td> {{ user.email }}</td>
      </tr>
    </table>

    <button @click="changeTitle">Change title</button>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      isCondition : true,
      message: `Lean on me`,
      users: [
        { id: 1, name: "Sajib", email: "sajib@sajib.com" },
        { id: 2, name: "Sajib2", email: "sajib2@sajib.com" },
        { id: 3, name: "Sajib3", email: "sajib3@sajib.com" },
        { id: 4, name: "Sajib4", email: "sajib4@sajib.com" },

      ]
    };
  },
  methods: {
    alertMe(){
      alert(`You remember me? --- James Moriatee`);
    },
    changeHardCode(){
      this.isCondition = !this.isCondition
    },
    changeTitle(){
      this.$emit('titleChange', 'You gonna miss me when I am gone.')
    }
    // loveSong(item){
    //   console.log(`love you like a love song baby -- ${item}`);
    // }
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
