<template>
  <div class="country-class" @click="clicked">Country: {{ name }}</div>
</template>

<script>
export default {
  name: "Country",
  props: ["name"],
  methods: {
    clicked() {
      this.$emit("clickBis", this.name);
    }
  }
};
</script>
