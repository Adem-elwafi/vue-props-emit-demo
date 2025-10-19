<template>
  <div>
    <h3>Child Component</h3>
    <p :style="{color: Color } ">{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: 'ChildDisplay',
  props: {
    text: {
      type: String,
      required: true
    },
  }
}
</script>

<style scoped>

</style>