<template>
  <section class="section">
    <div class="field">
     <div class="control">
      <input class="input is-primary" type="text" placeholder="TODOを追加してください" v-model="todo">
     </div>
    </div>
    <a class="button is-primary" @click="addTodo">追加</a>
  </section>
</template>

<script>
  export default {
    name: 'addForm',
    data: function () {
      return { todo: "" }
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
