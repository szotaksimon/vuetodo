<template>
  <div id="app">
    <Todo :todos="todos" @todo-item-changed="Changed"/>
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
  },
  methods: {
    Changed(e) {
      this.todos.map(function (todo) {
        if (todo.title != e.original) {
          return todo
        }
        todo.title = e.new
        return todo
      })
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
