<template>
  <li>
      <div v-if="!edit">
        {{title}}
        <button @click="Edit">Edit</button>
      </div>
      <div v-if="edit">
          <input type="text">
          <button @click="Save">Save</button>
      </div>
  </li>
</template>

<script>
export default {
    props: ['title'],
    data() {
        return {
            edit: false,
        }
    },
    methods: {
        Edit() {
            this.edit = true
        },
        Save() {
            this.edit = false
        }
    }
}
</script>

<style>

</style>