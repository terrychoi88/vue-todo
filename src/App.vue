<template>
    <div id="app">
      <todo-header></todo-header>
      <todo-input></todo-input>
      <todo-list></todo-list>
      <todo-footer></todo-footer>
    </div>
</template>

<script>
import TodoFooterVue from './components/TodoFooter.vue'
import TodoHeaderVue from './components/TodoHeader.vue'
import TodoInputVue from './components/TodoInput.vue'
import TodoListVue from './components/TodoList.vue'

export default {
    components: {
      'TodoHeader' : TodoHeaderVue,
      'TodoInput' : TodoInputVue,
      'TodoList' : TodoListVue,
      'TodoFooter' : TodoFooterVue
    }
}
</script>

<style>

</style>