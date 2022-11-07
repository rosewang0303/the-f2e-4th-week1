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

<style lang="scss">
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
      font-size: 36px;
      line-height: 42px;
      color: $white;
      margin-bottom: 31px;
      @include flexCenter;
      text-align: center;
      div {
        @include animateTyping();
      }
    }
    img {
      width: 164px;
      height: 66px;
      margin: 0 auto;
    }
  }
</style>
