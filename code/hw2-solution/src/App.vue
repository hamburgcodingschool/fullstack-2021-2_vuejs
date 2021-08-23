<template>
  <div id="fancyWrapper">
    <FancyInputHandler value="10" />
    <FancyInputHandler value="20" />
    <FancyInputHandler value="30" />
    <FancyInputHandler value="40" />
    <FancyInputHandler value="50" />
  </div>
</template>

<script>
import FancyInputHandler from "./components/FancyInputHandler.vue";

export default {
  name: "App",
  components: {
    FancyInputHandler,
  },
};
</script>

<style scoped>
#fancyWrapper {
  margin: 10px auto;
  width: 60%;
  background-color: #ebebeb;
  padding: 80px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  border-radius: 10px;
}
</style>
