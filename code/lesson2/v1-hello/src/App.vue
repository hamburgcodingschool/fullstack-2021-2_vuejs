<template>
  <CTAButton @onClick="defaultClicked" />
  <CTAButton type="cancel" title="Cancel" @onClick="cancelClicked" />
  <CTAButton type="confirm" title="OK" />
  <CTAButton type="abort" title="😱" />

  <Counter :value="counter" />
</template>

<script>
import CTAButton from "./components/CTAButton.vue";
import Counter from "./components/Counter.vue";

export default {
  name: "App",
  components: {
    CTAButton,
    Counter,
  },
  data: function () {
    return {
      counter: 0,
    };
  },
  methods: {
    defaultClicked: function (payload) {
      this.counter++;
      console.log(this.counter);
      console.log(payload);
      console.log("SOMETHING HAPPENED!");
    },
    cancelClicked: function () {
      console.log("MAKE SOMETHING GO BOOM!");
    },
  },
};
</script>

<style scoped></style>
