<template>
  <div>
      <ul>
          <TodoItem
          v-for="todo in todos"
          v-bind:key="todo.title"
          :title="todo.title"
          />
      </ul>
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue'
export default {
    props: ['todos'],
    components: {TodoItem}

}
</script>

