<template>
  <div>
      <ul>
          <li
          v-for="todo in todos"
          v-bind:key="todo.title"
          >{{ todo.title }}</li>
      </ul>
  </div>
</template>

<script>
export default {
    props: ['todos']

}
</script>

