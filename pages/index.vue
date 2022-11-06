<template>
  <div class="index">
    <span class="text" data-storke="index 測試">index 測試</span>
  </div>
</template>

<script>
export default {
  name: 'Index',
}
</script>

<style lang="scss">
  // index
  .index {
    font-family: 'Cubic';
    background-color: $black;
    color: $white;
    @include screenMD {
    }
    @include screenSM {
    }
    .text {
      font-size: 36px;
      line-height: 42px;
      @include textStroke();
    }
  }
</style>
