<template>
  <div id="app">
    <Card :todos="todos"/>
  </div>
</template>

<script>
import axios  from "axios";
import Card from './components/Card.vue';

export default {
  name: 'App',
  components: {
    Card
  },

  data(){
    return{
      todos:[],
    };
  },

  created(){
    axios.get(`https://jsonplaceholder.typicode.com/todos/`)
         .then(res=>{
          this.todos = res.data
         })
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
