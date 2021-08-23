<template>
  <input type="text" :value="value" readonly />
</template>

<script>
export default {
  props: {
    value: { default: 0 },
  },
};
</script>

<style scoped>
input {
  width: 100%;
  padding: 15px;
  border: solid 1px #afa8a8;
  border-radius: 5px;
}
</style>
