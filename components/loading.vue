<template>
  <div class="loading">
    <div class="loading__wrap">
      <div>
        <div class="loading__text">
          <div>Loading...</div>
        </div>
        <img src="@/assets/img/tank_1.gif" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoadIng',
}
</script>

<style lang="scss" scoped>
  .loading {
    background-color: $black;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    z-index: 1;
    @include flexCenter;
    &__wrap {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 50%;
    }
    &__text {
      margin-bottom: 0.31rem;
      @include flexCenter;
      text-align: center;
      div {
        font-size: 0.36rem;
        line-height: 0.42rem;
        color: $white;
        @include animateTyping();
      }
    }
    img {
      width: 1.64rem;
      height: 0.66rem;
      margin: 0 auto;
    }
  }
</style>
