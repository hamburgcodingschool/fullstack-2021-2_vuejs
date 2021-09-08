<template>
  <div class="detailContainer">
    <div v-if="apiResponseData.name">
      {{ apiResponseData.name }}
      <br />
      <br />
      {{ speciesData }}
    </div>
    <div v-else>Click something on the left...</div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      apiResponseData: {},
      speciesData: {},
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

        const speciesResponse = await fetch(this.apiResponseData.species.url);
        const speciesResult = await speciesResponse.json();

        this.speciesData = speciesResult;
      } catch (error) {
        console.log(error);
      }
    },
    // pokemon: function () {
    //   const context = this;
    //   fetch(this.pokemon.url)
    //     .then(function (response) {
    //       response
    //         .json()
    //         .then(function (result) {
    //           context.apiResponseData = result;
    //           const speciesURL = context.apiResponseData.species.url;
    //           fetch(speciesURL)
    //             .then(function (response) {
    //               response
    //                 .json(function (result) {
    //                   context.speciesData = result;
    //                 })
    //                 .catch(function (error) {
    //                   console.log(error);
    //                 });
    //             })
    //             .catch(function (error) {
    //               console.log(error);
    //             });
    //         })
    //         .catch(function (error) {
    //           console.log(error);
    //         });
    //     })
    //     .catch(function (error) {
    //       console.log(error);
    //     });
    // },
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
