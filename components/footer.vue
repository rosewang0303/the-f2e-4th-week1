<template>
  <div class="footer container">
    <div>
      <div class="footer__text">Design：小菜 / Frond End：蘿絲</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FooterView',

  data() {
    return {
    }
  },
}
</script>

<style lang="scss" scoped>
  .footer {
    background-color: $black;
    padding: 50px;
    > div {
      @include flexCenter;
    }
    &__text {
      font-size: 0.3rem;
    }
  }
</style>
