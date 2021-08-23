<template>
  <div id="fancyDiv">
    <FancySlider
      :value="sliderValue"
      @onInput="sliderChanged"
      class="fancySlider"
    />
    <FancyInput :value="sliderValue" class="fancyInput" />
  </div>
</template>

<script>
import FancySlider from "./FancySlider.vue";
import FancyInput from "./FancyInput.vue";

export default {
  components: {
    FancySlider,
    FancyInput,
  },
  props: {
    value: {
      default: 50,
    },
  },
  data: function () {
    return {
      sliderValue: this.value,
    };
  },
  methods: {
    sliderChanged: function (newValue) {
      this.sliderValue = newValue;
    },
  },
};
</script>

<style scoped>
#fancyDiv {
  display: flex;
  align-items: center;
  gap: 10px;
}

.fancySlider {
  flex: auto;
}

.fancyInput {
  width: 40px;
}
</style>
