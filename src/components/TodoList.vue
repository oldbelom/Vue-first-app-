<template>
  <div>
    <ul>
      <Todoitem
        v-for="todo of todos"
        v-bind:todo="todo"
      />
    </ul>
  </div>
</template>

<script>
import Todoitem from '@/components/Todoitem' 
export default {
  props: ['todos'], 
  components: {
    Todoitem
  }
}
</script>

<style>
  .list-item {
    width: 100px;
  }
</style>