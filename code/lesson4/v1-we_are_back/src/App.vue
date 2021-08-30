<template>
  <SimpleComponent name="Helder" city="Porto" />
  <SimpleComponent />
</template>

<script>
import SimpleComponent from "./components/SimpleComponent.vue";

export default {
  components: {
    SimpleComponent,
  },
};
</script>

<style>
body {
  background-color: #666;
}
</style>
