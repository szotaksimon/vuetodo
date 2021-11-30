<template>
  <li>
      <div v-if="!edit">
        {{title}}
        <button @click="Edit">Edit</button>
      </div>
      <div v-if="edit">
          <input type="text" v-model="title">
          <button @click="Save">Save</button>
      </div>
  </li>
</template>

<script>
export default {
    props: ['todo'],
    data() {
        return {
            title: this.todo.title,
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
                    title: this.title
                    },
            })
        }
    }
}
</script>

<style>

</style>