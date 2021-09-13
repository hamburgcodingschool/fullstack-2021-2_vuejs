<template>
  <h1>USer</h1>
  <p>{{ id }}</p>
</template>

<script>
export default {
  props: ["id"],
  mounted: function () {
    alert(this.id);
    // fetch some data from an api (or wherever really) based on the prop
    // that was actually consumed from the endpoint as stated in
    // router/index.js
  },
};
</script>

<style></style>
