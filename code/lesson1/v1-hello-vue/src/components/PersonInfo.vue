<template>
  <div>
    <p>{{ name }}</p>
    <p>{{ city }}</p>
  </div>
</template>

<script>
export default {
  props: ["name", "city"]
};
</script>
