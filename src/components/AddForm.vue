<template>
  <section class="section">
    <div class="field">
     <div class="control">
      <input class="input is-primary" type="text" placeholder="Primary input" v-model="todo">
     </div>
    </div>
    <a class="button is-primary" @click="$emit(todo)">Primary</a>
  </section>
</template>

<script>
  export default {
    name: 'addForm',
    data: function () {
      return { todo: "" }
    }
  }
</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";
</style>
