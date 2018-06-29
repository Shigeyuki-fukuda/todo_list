<template>
 <section class="section">
   <AddForm></AddForm>
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
    addTask(text) {
      this.todos.push({ todo: text })
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bulma/bulma.sass"; /* 追加 */
</style>
