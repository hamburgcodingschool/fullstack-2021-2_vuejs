<template>
  <div>
    <div class="result">
      The current greeting message is {{ apiResponseData.greeting }}
    </div>
    <button @click="handleRootClick">GO fetch from the `/` endpoint</button>
    <button @click="handleByeClick">GO fetch from the `/bye` endpoint</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      apiResponseData: {},
    };
  },
  methods: {
    fetchData: async function (url) {
      try {
        const response = await fetch(url);
        const result = await response.json();

        this.apiResponseData = result;
      } catch (error) {
        console.log(error);
      }
    },
    handleRootClick: function () {
      const url = `http://localhost:3000`;
      this.fetchData(url);
    },
    handleByeClick: function () {
      const url = `http://localhost:3000/bye`;
      this.fetchData(url);
    },
  },
};
</script>

<style scoped>
.result {
  width: 500px;
  min-height: 100px;
  border: solid 2px black;
}
</style>
