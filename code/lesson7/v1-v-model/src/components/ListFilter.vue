<template>
  <div>
    <input v-model="searchText" />
    <button @click="handleClearClick">clear</button>
    <ul>
      <li v-for="(name, i) in filteredNames" :key="i">{{ name }}</li>
    </ul>
  </div>
</template>

<script>
const names = [
  "Helder",
  "Siggi",
  "Flavia",
  "Janek",
  "Hannah",
  "Bob",
  "Joe",
  "Barbara",
];

export default {
  data: function () {
    return {
      filteredNames: names,
      searchText: "",
    };
  },
  methods: {
    handleClearClick: function () {
      this.searchText = "";
    },
  },
  watch: {
    searchText: function () {
      const context = this;
      this.filteredNames = names.filter(function (elem) {
        return elem.includes(context.searchText);
      });
    },
  },
};
</script>

<style scoped></style>
