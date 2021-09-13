<template>
  <div>
    <button
      @click="handleClickStop"
      :class="{ active: currentValue === 'STOP' }"
    >
      STOP
    </button>
    <button @click="handleClickGo" :class="{ active: currentValue === 'GO' }">
      GO
    </button>
  </div>
</template>

<script>
export default {
  emits: ["update:modelValue"],
  props: {
    modelValue: {
      type: String,
    },
  },
  data: function () {
    return {
      currentValue: this.modelValue,
    };
  },
  methods: {
    handleClickStop: function () {
      this.currentValue = "STOP";
      this.$emit("update:modelValue", this.currentValue);
    },
    handleClickGo: function () {
      this.currentValue = "GO";
      this.$emit("update:modelValue", this.currentValue);
    },
  },
};
</script>

<style scoped>
button {
  background-color: lightgray;
}
.active {
  background-color: burlywood;
}
</style>
