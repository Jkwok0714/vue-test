<template>
  <div>
    <p>Completed Tasks: {{todos.filter(todo => {return todo.done === true}).length}}</p>
    <p>Pending Tasks: {{todos.filter(todo => {return todo.done === false}).length}}</p>
    <TodoItem v-for="todo in todos" v-bind:todo="todo" v-bind:key="todo.title"></TodoItem>
  </div>
</template>

<script type = "text/javascript" >

import TodoItem from './TodoItem';

export default {
  props: ['todos'],
  components: {
    TodoItem,
  },
};
</script>

<style>
</style>
