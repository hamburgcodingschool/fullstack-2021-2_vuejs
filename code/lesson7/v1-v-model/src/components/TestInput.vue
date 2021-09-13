<template>
  <div>
    <input v-model="theText" />
    <br />
    Echo: {{ theText }}

    <br />
    <br />
    <button @click="handleResetClick">Reset text</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      theText: "Sample",
    };
  },
  methods: {
    handleResetClick: function () {
      this.theText = "Empty Text...";
    },
  },
};
</script>

<style scoped></style>
