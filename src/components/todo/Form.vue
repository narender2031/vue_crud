<template>
  <div>
    <b-row class="justify-content-center my-5">
      <b-form class="col-7" @submit="onSubmit">
        <b-form-group label-cols-sm="3" label="Title:" label-for="title">
          <b-form-input
            id="todo-title"
            type="text"
            placeholder="Title"
            v-model="form.title"
            required
          ></b-form-input>
        </b-form-group>
        <b-form-group label-cols-sm="3" label="description:" label-for="description">
          <b-form-textarea
            id="todo-description"
            placeholder="Enter something..."
            rows="3"
            v-model="form.description"
            max-rows="6"
            required
          ></b-form-textarea>
        </b-form-group>
        <b-button type="submit" variant="primary">Submit</b-button>
      </b-form>
    </b-row>
  </div>
</template>


<script>
import { type } from 'os';
export default {
  props: {
    todos: {
      type: Array
    }
  },
  data() {
    return {
      form: {
        title: "",
        description: ""
      },
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      let id = this.todos.length;
      let todo = {
        title: this.form.title,
        description: this.form.description,
        id: id + 1
      };
      this.todos.unshift(todo)
      this.form.title = "";
      this.form.description = "";
    }
  }
};
</script>