<template>
  <TodoComponent :todos="todos"/>
  
</template>

<script>
import TodoComponent from '../components/TodoComponent.vue';
export default {
  name: 'HomeView',
  data(){
    return {
      todos : ["Learn vue.js", "Learn Laravel", "Learn Django"]
      //send the list of todos to TodosComponent
    }
  },
  components: {
    TodoComponent
  }

}
</script>

<style>

</style>