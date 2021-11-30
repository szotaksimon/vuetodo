<template>
  <div id="app">
    <Todo :todos="todos"/>
  </div>
</template>

<script>
import Todo from './components/Todo.vue'

export default {
  name: 'App',
  components: {
    Todo
  },
  data() {
    return {
      todos: [
        {
          title: 'Első teendő'
        },
        {
          title: 'Második teendő'
        },
        {
          title: 'Harmadik teendő'
        },
        ]
    }
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
