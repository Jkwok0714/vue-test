<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Todo v-bind:todos="todos" />
  </div>
</template>

<script>
import Todo from './components/Todo';

export default {
  name: 'App',
  components: {
    Todo,
  },
  data() {
    return {
      todos: [{
        title: 'Go to Nippon',
        project: 'Travel',
        done: true,
      }, {
        title: 'Record Revelation by Insomnium',
        project: 'Metal Covers',
        done: false,
      }, {
        title: 'Write new song',
        project: 'Valkaron Band',
        done: false,
      }, {
        title: 'Paint Tomoko',
        project: 'Custom RG',
        done: false,
      }],
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
