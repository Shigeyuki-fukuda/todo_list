<template>
  <section class="section">
    <div class="field">
     <div class="control">
      <input class="input is-primary" type="text" placeholder="Primary input" v-model="task">
     </div>
    </div>
    <a class="button is-primary" @click="$emit(task)">Primary</a>
  </section>
</template>

<script>
  export default {
    name: 'addForm',
    data: function () {
      return { task: "" }
    }
  }
</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";
</style>
