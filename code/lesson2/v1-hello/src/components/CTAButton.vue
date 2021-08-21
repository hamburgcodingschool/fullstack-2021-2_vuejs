<template>
  <!-- <button v-bind:class="type" v-on:click="onClick">{{ title }}</button> -->
  <button :class="type" @click="clicked">{{ title }}</button>
</template>

<script>
export default {
  emits: ["onClick"],
  props: {
    title: {
      type: String,
      default: "Default",
    },
    type: {
      type: String,
      default: "",
    },
  },
  methods: {
    // onClick: function (event) {
    //   console.log(`${this.title} button was Clicked!!!!!`);
    //   this.$emit("clicked", {
    //     type: this.type,
    //     title: this.title,
    //     event: event,
    //   });

    // },
    clicked: function () {
      this.$emit("onClick", this.title);
    },
  },
};
</script>

<style scoped>
button {
  color: black;
  background-color: rgb(239, 239, 239);

  border: solid 3px black;
  border-radius: 15px;

  font-size: 24px;
  font-weight: bold;

  padding: 25px;

  box-shadow: 5px 5px 10px gray;
}

.cancel {
  color: green;
  border-color: green;
  box-shadow: 5px 5px 10px greenyellow;
  background-color: greenyellow;
}

.abort {
  color: orange;
  border-color: orange;
  box-shadow: 5px 5px 10px red;
  background-color: red;
}

.confirm {
  color: blue;
  border-color: blue;
  box-shadow: 5px 5px 10px aliceblue;
  background-color: aliceblue;
}
</style>
