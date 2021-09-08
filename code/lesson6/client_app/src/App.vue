<template>
  <div>
    <First />
    <ListPeople />
    <NewPerson />
  </div>
</template>

<script>
import First from "./components/First.vue";
import ListPeople from "./components/ListPeople.vue";
import NewPerson from "./components/NewPerson.vue";

export default {
  name: "App",
  components: { First, ListPeople, NewPerson },
};
</script>

<style></style>
