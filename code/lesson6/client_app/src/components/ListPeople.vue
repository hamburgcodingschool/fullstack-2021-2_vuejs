<template>
  <div>
    <div v-for="(person, i) in apiResponseData" :key="i">
      {{ person }}
      <!-- <br />
      {{ person.city }}
      <br />
      <br /> -->
    </div>
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
    fetchPeople: async function () {
      try {
        const url = `http://localhost:3000/api`;
        const response = await fetch(url);
        const result = await response.json();

        this.apiResponseData = result;
      } catch (error) {
        console.log(error);
      }
    },
  },
  mounted: function () {
    this.fetchPeople();
  },
};
</script>

<style scoped></style>
