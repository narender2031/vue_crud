<template>
  <div class="todo">
    <b-container>
      <todo-form :todos="todos" ></todo-form>
      <todo-list :todos="todos"></todo-list>
    </b-container>
  </div>
</template>

<script>
import TodoForm from '../components/todo/Form'
import TodoList from '../components/todo/List'
const TODOS = []

export default {
  components: {
    TodoForm,
    TodoList
  },
  data() {
    return {
      todos: TODOS
    }
  },
  methods: {}
}
</script>