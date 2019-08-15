<template>
  <b-row>
    <b-col>
      <p>Name: {{ info.name }}</p>
      <p>Email: {{ info.email }}</p>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: {
    info: { type: Object }
  }
};
</script>
