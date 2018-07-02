<template>
 <section class="section">
   <AddForm @addTodo="addTodo" v-bind:todos="todos"></AddForm>
  </section>
</template>

<script>
import AddForm from './components/AddForm.vue'

export default {
  name: 'app',
  components: {
    AddForm
  },
  data: function () {
    return { todos: [] }
  },
  methods: {
    addTodo(text) {
      this.todos.push(text)
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bulma/bulma.sass"; /* 追加 */
</style>
