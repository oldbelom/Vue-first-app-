<template>
  <div id="app">
    <h1>Todo application</h1>
    <hr>
    <TodoList
      v-bind:todos="todos"
    />
  </div>
</template>

<script>
import TodoList from '@/components/TodoList' 
export default {
  name: 'app',
  data() {
    return {
      todos: [
        {id: 1, title: 'Купить хлеб', comleted: false},
        {id: 2, title: 'Купить молоко', comleted: false},
        {id: 3, title: 'Купить пицуню', comleted: false}
      ]
    }
  },
  components: {
    TodoList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
