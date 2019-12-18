<template>
  <div class="countires-class">
    <Country
      v-for="countryName in list"
      :key="countryName"
      :name="countryName"
      @click.native="() => removeCountry(countryName)"
      @clickBis="argName => removeCountry(argName)"
    />
  </div>
</template>

<script>
/* eslint-disable no-console */
/* eslint-disable vue/no-unused-components */
import Country from "./Country";

export default {
  name: "Countries",
  components: { Country },
  props: ["list", "removeCountry"],
  created() {
    console.log("++", this.list);
  }
};
</script>
