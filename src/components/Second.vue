<template>
  <div>
    <h3 v-for="user in users" :key="user.id"> {{ user.name }} </h3>
  </div>
</template>

<script>
  export default{
    name: 'second',
    props: ['users']
  }

</script>

<style scoped>



</style>