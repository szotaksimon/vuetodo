<template>
  <li>
      <div v-if="!edit">
        {{text}}
        <button @click="Edit">Edit</button>
      </div>
      <div v-if="edit">
          <input type="text" v-model="text">
          <button @click="Save">Save</button>
      </div>
  </li>
</template>

<script>
export default {
    props: ['todo'],
    data() {
        return {
            text: this.todo.title,
            edit: false,
        }
    },
    methods: {
        Edit() {
            this.edit = true
        },
        Save() {
            this.edit = false
            this.$emit('todo-item-changed', {
                original: this.todo,
                new: {
                    title: this.text
                    },
            })
        }
    }
}
</script>

<style>

</style>