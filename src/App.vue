<template>
  <div>
    {{ cValue }}
    <p>Can't return to zero</p>
    <vue-slider @change="doSomethingWithVal" :min="-1" :max="4" />
  </div>
</template>

<script>
import VueSlider from "vue-slider-component";
import "vue-slider-component/theme/antd.css";
export default {
  name: "App",
  components: {
    VueSlider,
  },

  data: function () {
    return {
      testValue: 2,
      cValue: 0,
    };
  },

  methods: {
    doSomethingWithVal: function (value) {
      this.cValue = value;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
