<template>
  <div id="app">
    <Header></Header>
    <AddTask @taskAdded="newTask"></AddTask>
    <TaskList @taskRemoved="removeTask" :tasks="tasks"></TaskList>
  </div>
</template>

<script>
import Header from './components/Header';
import TaskList from './components/TaskList';
import AddTask from './components/AddTask';

export default {
  data: function() {
        return {
            tasks: []
        }
    },
  methods: {
    newTask(task) {
      this.tasks.push(task);
    },
    removeTask(index) {
      this.tasks.splice(index, 1);
    }
  },
  name: 'App',
  components: {
    Header,
    TaskList,
    AddTask
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
