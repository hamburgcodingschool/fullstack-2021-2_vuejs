<template>
  <div id="fancyWrapper">
    <FancyInputHandler value="0" />
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

// Create a new Vue Project
// That project should show if a "Switch" component is On or Off
// Create 1 component for the Switch
// Create 1 component for the On/Off display (simple text will do)
// Create a parent component so that you can add as many as you want anywhere to App for instance
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
