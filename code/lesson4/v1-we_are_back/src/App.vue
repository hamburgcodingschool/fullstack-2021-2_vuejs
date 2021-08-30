<template>
  <SimpleComponent name="Helder" city="Porto" />
  <SimpleComponent name="Bob" city="x" />
  <SimpleComponent name="Joe" :warning="true" />

  <ColorComponent :colors="['red', 'green']" />
  <ColorComponent :colors="list1" />
  <ColorComponent :colors="list2" />
</template>

<script>
import SimpleComponent from "./components/SimpleComponent.vue";
import ColorComponent from "./components/ColorComponent.vue";

// EXERCISE:
// 1 - Create a new component Color component
// 2 - that component should receive an array of colors as a prop. Ex: ["red", "green", "#000"]
// 2.1 - For each element in the array create a circle
// 2.2 - The circle should have the respective color
// 3 - The component should display in a row a circle for each color in the prop
// 4 - Odd circles should have a black border, Even circles should have a grey border
// 5 - Show the name of the color inside the circle

export default {
  components: {
    SimpleComponent,
    ColorComponent,
  },
  data: function () {
    return {
      list1: ["red", "green", "#00f"],
      list2: ["yellow", "pink", "grey", "#ac345a"],
    };
  },
};
</script>

<style>
body {
  background-color: #666;
}
</style>
