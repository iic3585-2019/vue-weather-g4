<template>
  <div class="scaleSelector selector">
    <v-select
      id="scales"
      v-model="inputtext"
      :items="scales"
      item-text="name"
      return-object
      background-color="#f88643"
      hide-details
      solo
    ></v-select>
  </div>
</template>

<script>
export default {
  name: "scales",
  data() {
    return {
      scales: [
        { name: "°F", param: "imperial" },
        { name: "°C", param: "metric" },
        { name: "K", param: "" }
      ]
    };
  },
  computed: {
    inputtext: {
      get() {
        return this.$store.state.scale.name;
      },
      set(value) {
        this.$store.dispatch("updateScale", value);
      }
    }
  }
};
</script>

<style>
.scaleSelector {
  width: 30%;
}
</style>

