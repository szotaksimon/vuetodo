<template>
  <div>
      <ul>
          <TodoItem
          v-for="todo in todos"
          v-bind:key="todo.title"
          :todo="todo"
          @todo-item-changed="Changed"
          />
      </ul>
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue'
export default {
    props: ['todos'],
    components: {TodoItem},
    methods: {
        Changed(e) {
            this.$emit('todo-item-changed', e)
        }
    }

}
</script>

