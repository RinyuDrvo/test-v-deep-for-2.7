<template>
  <button class="hoge-button">
    <hoge-svg v-if="isSvg" />
    <hoge-i v-else />
    ボタン
  </button>
</template>

<script>
import HogeSvg from "./HogeSvg.vue";
import HogeI from "./HogeI.vue";

export default {
  name: "HogeButton",
  components: {
    HogeSvg,
    HogeI,
  },
  props: {
    isSvg: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
.hoge-button {
  & ::v-deep svg path,
  i {
    fill: #fff;
  }

  // 上記と等価
  & :deep(svg path),
  i {
    fill: #fff;
  }

  /** 下記は等価ではない */
  // & :deep(svg path, i) {
  //   fill: #fff;
  // }

  // :deep(svg path),
  // :deep(i) {
  //   fill: #fff;
  // }
}
</style>
