<template>
<div class="container">
<div class="row">
<div class="col-sm-3" v-for="todo of todos"  
  v-bind:key="todo.id">
  <div class="card text-white bg-dark mb-3" 
  style="max-width: 18rem;" >
  <div class="card-body">
    <h5 class="card-title">{{todo.title}}</h5>
    <p class="text-success " v-if="todo.completed==true">Completed <i class="fa fa-check-circle fa-2x" aria-hidden="true"></i></p>
    <p class="text-danger " v-else>Not Completed <i i class="fa fa-close fa-2x" aria-hidden="true"></i> </p>
  </div>  
  </div>
</div>
</div>
</div>
</template>

<script>
export default {
  name: 'Card',
  props:['todos']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
