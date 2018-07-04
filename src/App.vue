<template>
 <section class="section">
   <AddForm @addTodo="addTodo"></AddForm>
   <ul>
     <TodoList @deleteTodo="deleteTodo" v-for="(todo, index) in todos"  v-bind:todo="{ name: todo.name, status: todo.status, index: index }"></TodoList>
   </ul>
  </section>
</template>

<script>
import AddForm from './components/AddForm.vue'
import TodoList from './components/TodoList.vue'

export default {
  name: 'app',
  components: {
    AddForm,
    TodoList
  },
  data: function () {
    return { todos: [] }
  },
  methods: {
    addTodo (text) {
      this.todos.push({
        name: text.name,
        status: false
      })
    },
    deleteTodo (index) {
      this.todos.splice(index, 1)
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bulma/bulma.sass"; /* 追加 */
</style>
