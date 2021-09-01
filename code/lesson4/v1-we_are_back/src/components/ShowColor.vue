<template>
  <div :style="{ backgroundColor: color }"></div>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "white",
    },
  },
};
</script>

<style scoped>
div {
  border: solid 5px black;
  height: 100px;
}
</style>
