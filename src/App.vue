<template>
  <div id="app">
    <div class="container">
      <hoge-button :is-svg="isSvg" class="hoge-button" />
      <button class="switch-button" @click="onClickChange">switch</button>
    </div>
  </div>
</template>

<script>
import HogeButton from "@/components/HogeButton.vue";

export default {
  name: "App",
  components: {
    HogeButton,
  },
  data() {
    return {
      isSvg: true,
    };
  },
  methods: {
    onClickChange() {
      this.isSvg = !this.isSvg;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>

<style scoped lanq="scss">
.container {
  display: flex;
  flex-direction: column;
}

.hoge-button {
  margin-bottom: 1rem;
}

/* .switch-button {
} */
</style>
