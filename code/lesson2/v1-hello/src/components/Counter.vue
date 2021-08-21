<template>
  <div>{{ value }}</div>
</template>

<script>
export default {
  props: {
    value: Number,
  },
};
</script>

<style scoped>
div {
  font-size: 40px;
}
</style>
