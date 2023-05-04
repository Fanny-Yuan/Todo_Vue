<template>
  <h1 className="slogan">Use this to manage your life and work</h1>
  <AddTodo />
  <TodoList />
  <CompletedList />
</template>

<script>
import AddTodo from './components/AddTodo.vue';
import TodoList from './components/TodoList.vue';
import CompletedList from './components/CompletedList.vue';

export default {
  name: 'App',
  components: {
    AddTodo,
    TodoList,
    CompletedList
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
