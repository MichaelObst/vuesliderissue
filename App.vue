<template>
  <div>
    {{ cValue }}
    <p>CVALUE ALWAYS PREVIOUS VALUE OF SLIDER</p>
    <HelloWorld v-model="testValue" @change="doSomethingWithVal()" />
  </div>
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
export default {
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
  },

  data: function () {
    return {
      testValue: 10,
      cValue: 0,
    };
  },

  methods: {
    doSomethingWithVal: function () {
      this.cValue = this.testValue;
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
