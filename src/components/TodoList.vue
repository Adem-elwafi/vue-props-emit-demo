<template>
  <ul>
    <li v-for="(todo, index) in todos" :key="index">
      {{ todo }}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'TodoList',
  props: {
    todos: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
ul {
  list-style: disc inside;
  padding-left: 1rem;
}
li {
  margin-bottom: 0.5rem;
}
</style>