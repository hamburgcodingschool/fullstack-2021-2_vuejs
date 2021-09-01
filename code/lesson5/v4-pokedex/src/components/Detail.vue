<template>
  <div class="detailContainer">{{ apiResponseData }}</div>
</template>

<script>
export default {
  data: function () {
    return {
      apiResponseData: {},
    };
  },
  props: {
    pokemon: {
      default: {},
    },
  },
  watch: {
    pokemon: async function () {
      try {
        const response = await fetch(this.pokemon.url);
        const result = await response.json();
        this.apiResponseData = result;
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>

<style scoped>
.detailContainer {
  background-color: antiquewhite;
  border: solid 2px black;
  width: 100%;
}
</style>
