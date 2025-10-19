<template>
  <div id="app">
    <h2>My Todo App</h2>
    <TodoInput @new-todo="addTodo" />
    <TodoList :todos="todos" />
  </div>
</template>

<script>
import TodoInput from './components/TodoInput.vue'
import TodoList from './components/TodoList.vue'

export default {
  name: 'App',
  components: { TodoInput, TodoList },
  data() {
    return {
      todos: []
    }
  },
  methods: {
    addTodo(todoText) {
      if (todoText && todoText.trim()) {
        this.todos.push(todoText.trim())
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  padding: 1rem;
}
</style>