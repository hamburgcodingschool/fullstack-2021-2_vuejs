<template>
  <div class="circleContainer">
    <!-- Color circles will go here -->
    <div
      v-for="(color, index) in colors"
      :key="index"
      class="circle"
      :style="{ 'background-color': color }"
    >
      {{ color }}
    </div>
  </div>
</template>

<script>
export default {
  emits: ["onSelectColor"],
  props: {
    colors: {
      type: Array,
      default: function () {
        return [];
      },
    },
  },
};
</script>

<style scoped>
.circleContainer {
  display: flex;
  flex-direction: row;
  gap: 10px;
}
.circle:nth-child(even) {
  border: solid 5px grey;
}
.circle {
  cursor: pointer;
  width: 60px;
  height: 60px;
  background-color: grey;
  border-radius: 50%;
  border: solid 5px black;
  text-align: center;
  line-height: 60px;
}
</style>
