<template>
  <main>
    <h1 className="slogan">Use this to manage your life and work</h1>
    <AddTodo />
    <TodoList />
    <CompletedList />
  </main>
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
body,
html,
ul,
ol,
h1,
p {
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  color: #343a40;
  background-color: #fff;
  line-height: 1.5;
}

* {
  box-sizing: border-box;
}

ul,
ol {
  list-style-type: none;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f9f9f9;
}

main {
  width: 1000px;
  min-width: 800px;
  height: 100%;
  display: flex;
  padding: 1rem 2.5rem;
  background-color: #fff;
  flex-direction: column;
  gap: 1rem;
}
main h1.slogan {
  text-align: center;
  font-size: 1.25rem;
  font-style: italic;
}

</style>
