<template>
  <div class="mainContainer">
    <List @onClick="handleClick" />
    <Detail :pokemon="chosenPokemon" />
  </div>
</template>

<script>
import List from "./components/List.vue";
import Detail from "./components/Detail.vue";

export default {
  name: "App",
  components: {
    List,
    Detail,
  },
  data: function () {
    return {
      chosenPokemon: {},
    };
  },
  methods: {
    handleClick: function (pokemon) {
      console.log(pokemon);
      this.chosenPokemon = pokemon;
    },
  },
};

// HOMEWORK:
// - Style it nicely...
// - As you style, consider creating smaller components if needed
// - Represnt some of the different values from the Pokemon in the Detail
// - Only image is mandatory
// - Add pagination to the List (Prev and Next buttons)
// - Buttons should only be enabled when there is a Next or Prev in the response
// - Make sure you understand the whole functionality, take time to understand properly
// - Have fun!
</script>

<style scoped>
.mainContainer {
  display: flex;
  flex-direction: row;
}
</style>
