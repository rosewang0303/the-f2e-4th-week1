<template>
  <div class="firm">
    <div class="container">
      <div class="firm__wrap">
        <div class="firm__title">
          <span>鑽石級</span>贊助商
        </div>
        <ul class="firm__item-wrap">
          <li class="firm__item">
            <img src="@/assets/img/firm_1.png" />
          </li>
          <li class="firm__item">
            <img src="@/assets/img/firm_2.png" />
          </li>
          <li class="firm__item">
            <img src="@/assets/img/firm_3.png" />
          </li>
        </ul>
      </div>
      <div class="firm__wrap">
        <div class="firm__title">共同推廣</div>
        <ul class="firm__item-wrap">
          <li class="firm__item">
            <img src="@/assets/img/firm_4.png" />
          </li>
          <li class="firm__item">
            <img src="@/assets/img/firm_5.png" />
          </li>
          <li class="firm__item">
            <img src="@/assets/img/firm_6.png" />
          </li>
        </ul>
      </div>
    </div>
    <div class="firm__diamond-wrap">
      <div
        v-for="(item, index) in diamondCount"
        :key="index"
        class="firm__diamond"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FirmView',

  data() {
    return {
      diamondCount: 17,
    }
  },
}
</script>

<style lang="scss" scoped>
  .firm {
    background-color: $primary;
    padding-top: 115px;
    padding-bottom: 250px;
    @include screenMD {
      padding-top: 49px;
      padding-bottom: 100px;
    }
    &__wrap {
      &:first-child {
        margin-bottom: 150px;
        .firm__item {
          img {
            width: 2.8961rem;
            height: 2.8961rem;
            @include screenMD {
              width: 1.5626rem;
              height: 1.5626rem;
            }
          }
        }
        @include screenMD {
          margin-bottom: 50px;
        }
      }
      &:nth-child(2) {
        .firm__item {
          &:nth-child(1) {
            img {
              width: 2.3994rem;
              height: 0.806rem;
              @include screenMD {
                width: 1.2946rem;
                height: 0.4349rem;
              }
            }
          }
          &:nth-child(2) {
            img {
              width: 2.6056rem;
              height: 0.806rem;
              @include screenMD {
                width: 1.4058rem;
                height: 0.4349rem;
              }
            }
          }
          &:nth-child(3) {
            img {
              width: 2.868rem;
              height: 1.1528rem;
              @include screenMD {
                width: 1.5474rem;
                height: 0.622rem;
              }
            }
          }
        }
      }
    }
    &__title {
      text-align: center;
      font-size: 0.72rem;
      line-height: 0.84rem;
      margin-bottom: 50px;
      @include screenMD {
        margin-bottom: 20px;
        font-size: 0.36rem;
        line-height: 0.42rem;
      }
      span {
        color: $yellow;
        @include screenMD {
          font-size: 0.36rem;
          line-height: 0.42rem;
        }
      }
    }
    &__item-wrap {
      @include flexCenter;
    }
    &__item {
      @include flexCenter;
      width: 374.9px;
      height: 374.9px;
      background-color: $white;
      margin: 0 15px;
      @include screenMD {
        width: 202.27px;
        height: 202.27px;
        margin: 0 9px;
      }
    }
    &__diamond-wrap {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
    }
    &__diamond {
      background-image: url('@/assets/img/diamond.png');
      background-repeat: no-repeat;
      background-size: contain;
      position: absolute;
      &:nth-child(1) {
        width: 28px;
        height: 24px;
        top: 51px;
        left: 38px;
      }
      &:nth-child(2) {
        width: 20px;
        height: 14px;
        top: 86px;
        left: 18px;
      }
      &:nth-child(3) {
        width: 64px;
        height: 47px;
        top: 80px;
        left: 195px;
      }
      &:nth-child(4) {
        width: 64px;
        height: 47px;
        top: 33px;
        right: 174px;
      }
      &:nth-child(5) {
        width: 38px;
        height: 28px;
        top: 66px;
        right: 57px;
      }
      &:nth-child(6) {
        width: 51px;
        height: 38px; 
        top: 403px;
        right: 76px;
      }
      &:nth-child(7) {
        width: 161px;
        height: 119px;
        left: 144px;
        top: 855px;
      }
      &:nth-child(8) {
        width: 51px;
        height: 38px;
        left: 624px;
        top: 765px;
      }
      &:nth-child(9) {
        width: 96px;
        height: 71px;
        left: 1249px;
        top: 705px;
      }
      &:nth-child(10) {
        width: 51px;
        height: 38px;
        left: 1654px;
        top: 974px;
      }
      &:nth-child(11) {
        width: 51px;
        height: 38px;
        left: 1818px;
        top: 1066px;
      }
      &:nth-child(12) {
        width: 96px;
        height: 71px;
        left: 96px;
        top: 1218px;
      }
      &:nth-child(13) {
        width: 51px;
        height: 38px;
        left: 45px;
        top: 1384px;
      }
      &:nth-child(14) {
        width: 96px;
        height: 71px;
        left: 649px;
        top: 1403px;
      }
      &:nth-child(15) {
        width: 161px;
        height: 119px;
        left: 1113px;
        top: 1289px;
      }
      &:nth-child(16) {
        width: 51px;
        height: 38px;
        left: 1581px;
        top: 1412px;
      }
      &:nth-child(17) {
        width: 96px;
        height: 71px;
        left: 1654px;
        top: 1360px;
      }
    }
  }
</style>
