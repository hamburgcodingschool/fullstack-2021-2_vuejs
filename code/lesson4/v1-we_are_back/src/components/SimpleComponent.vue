<template>
  <!-- <p v-if="city === 'Porto'">Hello I am {{ name }} and I am from {{ city }}</p>
  <p v-else-if="city">Hello I am {{ name }} and I am from {{ city }} 😭</p>
  <p v-else>Hello I am {{ name }}</p> -->

  <!-- <p :class="{ warningParagraph: warning === true }"></p> -->
  <p :class="{ warningParagraph: warning }">
    Hello I am {{ name }}
    <span v-if="city">and I am from {{ city }}</span>
  </p>
</template>

<script>
// EXERCISE
// 1 - Use v-if to only show the second sentence when the city is present (not undefined)
// 2 - add a new Boolean prop `Warning` change the background to Yellow if `Warning` is true

export default {
  props: {
    warning: {
      type: Boolean,
      default: false,
    },
    name: {
      default: "Default name!",
    },
    city: String,
  },
};
</script>

<style scoped>
.warningParagraph {
  background-color: yellow;
  color: red;
}

p {
  color: lime;
  background-color: green;

  padding: 20px;
  margin: 0 0 20px 0;
}
</style>
