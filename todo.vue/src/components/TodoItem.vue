<template>
    <li>
      <input type="checkbox" :checked="todo.done" />
      <label data-id={id}>{{todo.title}}</label>
      <i class="bi-trash" data-id={id} ></i>
    </li>
</template>

<script>
  export default {
    name:"TodoItem",
    props:["todo"],
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

li {
  display: flex;
  align-items: center;
  list-style: none;
  height: 2.5rem;
  line-height: 2.5rem;
  background-color: #f9f9f9;
  border-radius: 3px;
  margin-bottom: 0.5rem;
  padding: 0 1rem;
  position: relative;
}
li input[type=checkbox] {
  transform: scale(1.2);
  margin-right: 0.5rem;
}
li input[type=checkbox]:checked + label {
  color: #a9a9a9;
  text-decoration: line-through;
}
li label {
  flex: 1;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
li .bi-trash {
  display: none;
  margin-left: 0.5rem;
  color: #f56969;
}
li:hover .bi-trash {
  display: block;
}

</style>