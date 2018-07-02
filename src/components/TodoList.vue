<template>
  <li>
    {{ todo.list }}
    <a class="button is-primary" @click="deleteTodo">削除</a>
  </li>
</template>

<script>
  export default {
    name: 'todoList',
    props: [
      'todo'
    ],
    methods: {
      deleteTodo: function () {
        this.$emit('deleteTodo', this.todo.index)
      }
    }
  }
</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";
</style>
