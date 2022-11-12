<template>
  <div class="index">
    <!-- <span class="text" data-storke="index 測試">index 測試</span> -->
    <Transition name="fade">
      <Loading v-if="loading" />
    </Transition>
    <Navbar />
    <Main />
    <Trouble />
    <!-- TODO mountain -->
    <Stage />
    <Faq />
    <Firm />
    <Footer />
  </div>
</template>

<script>
export default {
  name: 'Index',

  data() {
    return {
      loading: true,
    }
  },

  mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 2500);
  },
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
