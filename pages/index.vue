<template>
  <div class="index">
    <div class="text" data-storke="index 測試">index 測試</div>
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
    @include screenMD {
    }
    @include screenSM {
    }
    .text {
      font-size: 36px;
      line-height: 42px;
      color: $white;
      @include textStroke();
    }
  }
</style>
