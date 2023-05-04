<template>
  <main>
    <h1 className="slogan">Use this to manage your life and work</h1>
    <AddTodo />
    <TodoList :todos="todos"/>
    <CompletedList :todos="todos"/>
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
  },
  data() {
    return {
      //由于todos是MyHeader组件和MyFooter组件都在使用，所以放在App中（状态提升）
      todos:[
        {id:'1',title:'task01',done:false},
        {id:'2',title:'task02',done:false},
        {id:'3',title:'task03',done:true},
        {id:'4',title:'task04',done:true}
      ]
    }
  },
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
