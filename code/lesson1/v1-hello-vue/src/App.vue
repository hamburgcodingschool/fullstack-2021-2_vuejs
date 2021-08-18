<template>
  <h1>My Awesome Vue page</h1>
  <p>The awesome people here today:</p>
  <ul>
    <li><PersonInfo name="Helder" city="Porto" /></li>
    <li><PersonInfo name="Siggi" city="Eutin" /></li>
    <li><PersonInfo name="Flavia" city="Pisa" /></li>
    <li><PersonInfo name="Janek" city="Göttingen" /></li>
  </ul>
</template>

<script>
import PersonInfo from "./components/PersonInfo.vue";

export default {
  components: {
    PersonInfo
  }
};
</script>

<style scoped>
h1 {
  background-color: aqua;
}

p {
  font-size: 30px;
  color: cadetblue;
}
</style>
