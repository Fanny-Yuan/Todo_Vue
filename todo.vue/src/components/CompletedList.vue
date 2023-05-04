<template>
    <h3>Completed</h3>
    <ul class="completed-list">
    <TodoItem 
        v-for="todoObj in completedTask"
        :key="todoObj.id" 
        :todo="todoObj"
        :checkTodo="checkTodo" 
        :deleteTodo="deleteTodo"
    />
  </ul>
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
  name: 'CompletedList',
  components: {TodoItem},
  props:["todos","checkTodo","deleteTodo"],
  computed:{
    completedTask(){
      return this.todos.filter((task)=>task.done);
    }
  }
}
</script>