<template>
  <div class="input-section">
    <input v-model="newTodo" @keyup.enter="submitTodo" placeholder="Add a todo" />
    <button @click="submitTodo">Add</button>
  </div>
</template>

<script>
export default {
  name: 'TodoInput',
  data() {
    return {
      newTodo: ''
    }
  },
  emits: ['new-todo'],
  methods: {
    submitTodo() {
      this.$emit('new-todo', this.newTodo)
      this.newTodo = ''
    }
  }
}
</script>

<style scoped>
.input-section {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 1rem;
}
input {
  flex: 1;
  padding: 0.4rem;
}
button {
  padding: 0.4rem 0.8rem;
  cursor: pointer;
}
</style>