<template>
  <li>
    <label class="checkbox" v-bind:class="{ done: todo.status }">
      <input type="checkbox" v-on:input="checkedTodo">
      {{ todo.name }}
    </label>
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
      },
      checkedTodo: function () {
        this.$emit('checkedTodo', this.todo.index)
      }
    }
  }
</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";
.done { text-decoration: line-through }
</style>
