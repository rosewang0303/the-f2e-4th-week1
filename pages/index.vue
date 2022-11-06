<template>
  <div class="index">
    <!-- <span class="text" data-storke="index 測試">index 測試</span> -->
    <Navbar />
  </div>
</template>

<script>
export default {
  name: 'Index',
}
</script>

<style lang="scss">
  .index {
    font-family: 'Cubic';
    background-color: $black;
    color: $white;
    @include screenLG {
    }
    @include screenMD {
    }
    // .text {
    //   font-size: 36px;
    //   line-height: 42px;
    //   @include textStroke();
    // }
  }
</style>
