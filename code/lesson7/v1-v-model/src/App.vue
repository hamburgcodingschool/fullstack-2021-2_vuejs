<template>
  <!-- <InputButtons v-model="inputText" />
  <DisplayResult :text="inputText" />
  <TestInput /> -->
  <ListFilter />
</template>

<script>
// import DisplayResult from "./components/DisplayResult.vue";
// import InputButtons from "./components/InputButtons.vue";
// import TestInput from "./components/TestInput.vue";
import ListFilter from "./components/ListFilter.vue";

export default {
  name: "App",
  components: {
    // InputButtons,
    // DisplayResult,
    // TestInput,
    ListFilter,
  },
  data: function () {
    return {
      inputText: "STOP",
    };
  },
};
</script>

<style scoped></style>
