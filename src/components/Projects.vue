<template>
  <b-container class="mt-5">
    <b-row>
      <b-col>
        <h1 class="h3">Projects</h1>
      </b-col>
    </b-row>
    <b-row class="mt-5">
      <b-col v-for="project in projects" v-bind:key="project.id">
        <h5>{{ project.title }}</h5>
        <p>{{ project.desc }}</p>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  props: {
    projects: { type: Array }
  }
};
</script>
