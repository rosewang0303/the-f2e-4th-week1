<template>
  <div class="event container">
    <div>
      <div
        class="event__step"
        :class="{ 'event__step--active': currentStep >= 0 }"
      >
        <div class="event__left">
          <div class="event__text-wrap">
            <div class="event__title">SIGN UP!</div>
            <div class="event__content">
              開放報名：<br/>
              10/13(四) 早上 11:00 - 11/6(日) 晚上 23:59<br/><br/>
              截止前可修改報名組別。<br/>
            </div>
          </div>
        </div>
        <div class="event__btn">
          <a href="https://2022.thef2e.com/signup" target="_blank">
            <button>點我註冊報名!</button>
          </a>
        </div>
      </div>
      <div class="event__step">
        <div class="event__left">
          <div class="event__text-wrap">
            <div class="event__title">START!</div>
            <div class="event__content">
              各組別開賽：<br/>
              UI組、團體組開賽 10/31、前端組開賽 11/7
            </div>
          </div>
        </div>
      </div>
      <div class="event__step">
        <div class="event__left">
          <div class="event__text-wrap">
            <div class="event__title">UPLOAD!</div>
            <div class="event__content">
              登陸作品：<br/>
              10/31(一) 中午 12:00 - 11/28(一) 中午 12:00
            </div>
          </div>
        </div>
      </div>
      <div class="event__step">
        <div class="event__left">
          <div class="event__text-wrap">
            <div class="event__title">STREAM!</div>
            <div class="event__content">
              資深開發者到來，直播分享零阻礙！<br/><br/>
              線上直播：<br/>
              11/3 - 11/24（每週四）
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventView',

  data() {
    return {
      currentStep: 0,
    }
  },
}
</script>

<style lang="scss" scoped>
  .event {
    padding-top: 300px;
    padding-bottom: 450px;
    margin: 0 87px;
    &__step {
      display: flex;
      align-items: flex-end;
      justify-content: space-between;
      flex-wrap: wrap;
      border-left: 5px dashed rgba(255, 255, 255, 0.5);
      padding-left: calc(70px + 140.8px / 2);
      padding-bottom: 324px;
      &:before {
        content: '';
        background-image: url("@/assets/img/flag_1.png");
        background-repeat: no-repeat;
        background-size: contain;
        width: 140.8px;
        height: 229px;
        position: absolute;
        left: calc(-70px - 140.8px / 4 + 15px);
        @include screenMD {
          width: 85.29px;
          height: 138.73px;
          left: calc(-70px - 85.29px / 4 + 35px);
        }
      }
      &--active {
        &:before {
          animation: 0.5s flag 0.6s ease both;
        }
      }
      .event__title {
          margin-bottom: 73px;
          @include screenMD {
            font-size: 0.36rem;
            line-height: 0.42rem;
          }
        }
      &:first-child,
      &:last-child {
        .event__title {
          margin-bottom: 0;
        }
      }
      &:last-child {
        padding-bottom: 0;
      }
    }
    &__left {

    }
    &__flag {

    }
    &__text-wrap {

    }
    &__title {
      color: $tertiary;
      font-size: 0.72rem;
      line-height: 0.84rem;
    }
    &__content {
      font-size: 0.24rem;
      line-height: 0.36rem;
      @include screenMD {
        font-size: 0.16rem;
        line-height: 0.24rem;
      }
    }
    &__btn {
      button {
        @include buttonLG;
      }
      @include screenSM {
        margin-top: 10px;
      }
    }
  }
</style>
