<template>
  <div class="main container">
    <div>
      <ul class="main__title">
        <li>I-    00</li>
        <li>HI- 99999</li>
        <li>Hex School</li>
      </ul>
      <img class="main__banner" src="@/assets/img/banner.png" />
      <ul class="main__options">
        <li :class="{ 'active': keyboard === 'up' }">
          <div class="tank"></div>
          <a
            href="https://2022.thef2e.com/login"
            target="_blank"
            class="text"
            @pointerover="keyboard = 'up'"
          >1  LOG IN</a>
        </li>
        <li :class="{ 'active': keyboard === 'down' }">
          <div class="tank"></div>
          <a
            href="https://2022.thef2e.com/signup"
            target="_blank"
            class="text"
            @pointerover="keyboard = 'down'"
          >2  SIGN UP</a>
        </li>
      </ul>
      <div class="main__subtitle">Interactive And Responsive Web Design.</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainView',

  data() {
    return {
      keyboard: 'up',
    }
  },

  mounted() {
    document.addEventListener('keydown', (event) => {
      if (event.code === 'ArrowUp') {
        this.keyboard = 'up';
      } else if (event.code === 'ArrowDown') {
        this.keyboard = 'down';
      }
    });
  },
}
</script>

<style lang="scss">
  .main {
    background-color: $black;
    @include flexCenter;
    padding-bottom: 327px;
    @include screenMD {
      padding-bottom: 253.31px;
    }
    &__title {
      width: 100%;
      @include flexCenterH;
      justify-content: space-between;
      margin-top: 24px;
      li {
        font-size: 36px;
        line-height: 42px;
        @include screenMD {
          font-size: 24px;
          line-height: 28px;
        }
      }
    }
    &__banner {
      width: 54.58%;
      margin: 113px auto 0 auto;
      @include screenMD {
        width: 76.69%;
        margin-top: 246px;
      }
    }
    &__options {
      margin-top: 109px;
      @include screenMD {
        margin-top: 87px;
      }
      li {
        @include flexCenter;
        &:first-child {
          margin-bottom: 24px;
        }
        .tank {
          width: 86px;
          height: 53px;
          background-image: unset;
          background-repeat: no-repeat;
          background-size: contain;
          @include screenMD {
            width: 68px;
            height: 42px;
          }
        }
        .text {
          cursor: pointer;
          display: block;
          font-size: 42px;
          line-height: 49px;
          color: $white;
          margin-left: 42px;
          width: 30%;
          white-space: nowrap;
          @include screenMD {
            margin-left: 34px;
            font-size: 36px;
            line-height: 42px;
            width: 40%;
          }
          @include screenSM {
            width: 50%;
          }
        }
        &.active {
          .tank {
            background-image: url('@/assets/img/tank_2.gif');
          }
          .text {
            color: $primary;
            animation: 0.8s twinkle 0.7s infinite;
            @keyframes twinkle {
              from { opacity: 0; }
              to { opacity: 1; }
            }
          }
        }
      }
    }
    &__subtitle {
      font-size: 36px;
      line-height: 42px;
      text-align: center;
      margin-top: 103px;
      @include screenMD {
        margin-top: 225px;
        font-size: 24px;
        line-height: 28px;
      }
    }
  }
</style>
