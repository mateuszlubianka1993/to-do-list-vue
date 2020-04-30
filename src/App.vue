<template>
  <div id="app">
    <Header></Header>
    <TaskList :tasks="tasks"></TaskList>
  </div>
</template>

<script>
import Header from './components/Header';
import TaskList from './components/TaskList';

export default {
  data: function() {
        return {
            tasks: [
              'Do something',
              'Do else',
              'XXX ',
              ' DDDDDDDDDDDDDDDDDDD'
            ]
        }
    },
  name: 'App',
  components: {
    Header,
    TaskList
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
}
</style>
