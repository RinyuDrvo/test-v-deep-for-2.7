<template>
  <button class="hogeButton">
    <svg>
      <path />
    </svg>
    <i></i>
    ボタン
  </button>
</template>

<script>
export default {
  name: "HogeButton",
};
</script>

<style scoped lang="scss">
.hogeButton {
  // & ::v-deep svg path,
  // i {
  //   fill: #fff;
  // }

  // 上記と等価
  & :deep(svg path),
  i {
    fill: #fff;
  }
}
</style>
