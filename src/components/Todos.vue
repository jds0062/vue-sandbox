<template>
  <div>
    <div v-for="item in todos" v-bind:key="item.id">
      <TodoItem v-bind:todo="item" v-on:delete-todo="$emit('delete-todo', item.id)"/>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "Todos",
  components: {
    TodoItem
  },
  props: ["todos"]
};
</script>

<style scoped>
</style>
