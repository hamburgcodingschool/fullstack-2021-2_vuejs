<template>
  <p>Hello I am {{ name }} and I am from {{ city }}</p>
  <p>Hello I am {{ name }}</p>
</template>

<script>
// EXERCISE
// Use v-if to only show the second sentence when the city is present (not undefined)

export default {
  props: {
    name: {
      default: "Default name!",
    },
    city: String,
  },
};
</script>

<style scoped>
p {
  color: lime;
  background-color: green;

  padding: 20px;
  margin: 0 0 20px 0;
}
</style>
