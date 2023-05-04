<template>
  <ul class="todo-list">
    <TodoItem 
      v-for="todoObj in todoTask"
			:key="todoObj.id" 
			:todo="todoObj" 
    />
  </ul>
    
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
  name: 'TodoList',
  components: {TodoItem},
  props:["todos"],
  computed:{
    todoTask(){
      return this.todos.filter((task)=>!task.done);
    }
  }
}
</script>