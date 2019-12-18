<template>
  <div id="app">
    <!-- {{ age }} -->
    <!-- <Countries :isMajor="isMajor" /> -->
    <Countries :list="countries" :removeCountry="removeOneCountry" />
    <button @click="add">click me</button>
  </div>
</template>

<script>
/* eslint-disable no-console */
import Countries from "./components/Countries";

export default {
  name: "app",
  data() {
    return {
      age: 10,
      // isMajor: false,
      countries: ["Belgium", "France", "Italy", "USA"]
    };
  },
  computed: {
    isMajor() {
      console.log("new", this.age);
      return this.age >= 18;
    }
  },
  watch: {
    // age(newValue, oldValue) {
    //   console.log("new", newValue);
    //   console.log("old", oldValue);
    //   this.isMajor = this.age >= 18;
    // }
  },
  components: { Countries },
  methods: {
    add() {
      this.age = this.age + 1;
    },
    removeOneCountry(countryName) {
      console.log("name", countryName);
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
