<template>
  <div>{{ number }}</div>
  <button v-on:click="goUpClicked">GO UP</button>
  <button v-on:click="goDownClicked">GO DOWN</button>
</template>

<script>
export default {
  data: function() {
    return {
      number: 0
    };
  },
  methods: {
    goUpClicked: function() {
      this.number++;
    },
    goDownClicked: function() {
      this.number--;
    }
  }
};
</script>

<style scoped>
div {
  height: 50px;
  width: 200px;
  background-color: pink;
  text-align: center;
  font-size: 40px;
}
</style>
