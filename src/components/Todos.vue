<template>
  <div>
    <div v-bind:key="todo.id" v-for="todo in todos">
      <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
    </div>  
  </div>
</template>

<script>
import TodoItem from '@/components/TodoItem.vue';

export default {
  names: 'Todos',
  components: {
    TodoItem
  },
  props: {
    todos: {
      type: Array,
      required: true
    }
  }
};
</script>

<style scoped>

</style>