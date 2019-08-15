<template>
  <div>
    <b-row v-if="todos.length > 0">
      <b-col cols="3">
        <div class="todo-list">
          <h4 class="my-4">
            <strong class="my-3">Todos</strong>
          </h4>
          <b-list-group>
            <b-list-group-item
              button
              v-for="todo in todos"
              v-bind:key="todo.id"
              @click="showDescription(todo.id)"
              :class="{active : selected ==  todo.id}"
            >{{ todo.title }}</b-list-group-item>
          </b-list-group>
        </div>
      </b-col>
      <b-col cols="7">
        <h4 class="my-4">
          <strong class="my-3">Description</strong>
        </h4>
        <P>{{ description == null ?  todos[0].description : description }}</P>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      description: null,
      selected: null
    }
  },
  props: {
    todos: {
      type: Array
    }
  },
  methods: {
    showDescription(todoID) {
      this.description = ""
      this.selected = ""
      this.selected = todoID
      let desc = this.description
      this.todos.filter(function(todo) {
        if (todo.id === todoID) {
          return desc = todo.description;
        }
      });
      this.description = desc
    },
    deleteTodo() {
      
    }
  }
};
</script>