<template>
  <ul class="todo-list">
    <TodoItem 
      v-for="todoObj in todoTask"
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
  name: 'TodoList',
  components: {TodoItem},
  props:["todos","checkTodo","deleteTodo"],
  computed:{
    todoTask(){
      return this.todos.filter((task)=>!task.done);
    }
  }
}
</script>