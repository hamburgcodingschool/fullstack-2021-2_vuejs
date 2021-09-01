<template>
  <div class="listContainer">
    <div v-for="(pokemon, i) in apiResponseData.results" :key="i">
      <span>{{ pokemon.name }}</span>
      <button @click="handleClick(pokemon)">Detail</button>
    </div>
  </div>
</template>

<script>
export default {
  emits: ["onClick"],
  data: function () {
    return {
      apiResponseData: {},
    };
  },
  mounted: async function () {
    const url = "https://pokeapi.co/api/v2/pokemon/";
    try {
      const response = await fetch(url);
      const result = await response.json();

      this.apiResponseData = result;
    } catch (error) {
      console.log(error);
    }
  },
  methods: {
    handleClick: function (pokemon) {
      this.$emit("onClick", pokemon);
    },
  },
};
</script>

<style scoped>
.listContainer {
  background-color: antiquewhite;
  border: solid 2px black;
  width: 100%;
}
</style>
