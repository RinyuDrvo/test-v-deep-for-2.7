<template>
  <div id="app">
    <hoge-button />
  </div>
</template>

<script>
import HogeButton from "@/components/HogeButton.vue";

export default {
  name: "App",
  components: {
    HogeButton,
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
