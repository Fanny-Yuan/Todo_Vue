<template>
    <h3>Completed</h3>
    <TodoItem />
    <TodoItem />
    <TodoItem />
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
  name: 'CompletedList',
  components: {
    TodoItem
}
}
</script>