<template>
  <section class="section">
    <div class="field">
     <div class="control">
      <input class="input is-primary" type="text" placeholder="TODOを追加してください" v-model="todo.name">
     </div>
    </div>
    <a class="button is-primary" @click="addTodo">追加</a>
  </section>
</template>

<script>
  export default {
    name: 'addForm',
    data: function () {
      return {
        todo: [ { name: "", status: false } ]
      }
    },
    methods: {
      addTodo: function () {
        this.$emit('addTodo', this.todo)
      }
    }
  }
</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";
</style>
