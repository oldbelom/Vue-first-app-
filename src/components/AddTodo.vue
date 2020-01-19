<template>
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="title">
    <button type="submit">Create</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: ''
    }
  },
  methods: {
    onSubmit() {
      console.log('Submit')
      if (this.title.trim()) {
        const newTodo = {
          id: Date.now(),
          title: this.title,
          completed: false
        }

        this.$emit('add-todo', newTodo)
        this.title = ''
      }
    }
  }
}
</script>

<style scoped>
  form {
    margin: 25px 0;
    display: flex;
    justify-content: center;
  }
  input {
    width: 400px;
  }
</style>