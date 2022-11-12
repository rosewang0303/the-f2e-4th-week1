<template>
  <div class="trouble">
    <div class="trouble__wrap">
      <div class="trouble__rect">
        <div class="trouble__webpage">
          <img class="trouble__tank" src="@/assets/img/tank_1.gif" />
          <div class="trouble__msg trouble__msg--1">
            <div>I’m cool !</div>
          </div>
        </div>
        <div
          class="trouble__title trouble__title--1"
          data-storke="羨慕別人的酷酷網頁動畫..."
        >羨慕別人的酷酷網頁動畫...</div>
      </div>
    </div>
    <div class="trouble__wrap">
      <div class="trouble__rect">
        <div class="trouble__soldier-wrap">
          <img class="trouble__soldier" src="@/assets/img/trouble_2_soldier.png" />
        </div>
        <div class="trouble__msg trouble__msg--2">
          <div>!@#$%...</div>
        </div>
        <div
          class="trouble__title trouble__title--2"
          data-storke="滿足不了同事的許願..."
        >滿足不了同事的許願...</div>
      </div>
    </div>
    <div class="trouble__wrap">
      <div class="trouble__rect">
        <img class="trouble__tree" src="@/assets/img/tree.png" />
        <img class="trouble__soldier-back" src="@/assets/img/trouble_3_soldier.png" />
        <div
          class="trouble__title trouble__title--3"
          data-storke="動畫技能樹太雜無從下手..."
        >動畫技能樹太雜無從下手...</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TroubleView',
}
</script>

<style lang="scss" scoped>
  .trouble {
    background-color: $black;
    padding-bottom: 23.43vw;
    @include screenMD {
      padding-bottom: 28vw;
    }
    &__wrap {
      @include flexCenterH;
      &:nth-child(1) {
         margin-bottom: 12.66vw;
        .trouble__rect {
          padding: 3.28vw 9.74vw 4.06vw 8.13vw;
          @include screenMD {
            padding: 6.51vw 0 7.94vw 0;
          }
        }
      }
      &:nth-child(2) {
        margin-bottom: 12.66vw;
        justify-content: flex-end;
      }
      @include screenMD {
        &:nth-child(1),
        &:nth-child(2) {
          margin-bottom: 28vw;
        }
      }
    }
    &__rect {
      width: 51.04vw;
      height: 29.69vw;
      background-color: $primary;
      @include flexCenterH;
      @include screenMD {
        width: 100vw;
        height: 58.2vw;
        display: block;
      }
    }
    &__webpage {
      width: 33.18vw;
      height: 22.34vw;
      background-image: url('@/assets/img/webpage.gif');
      background-repeat: no-repeat;
      background-size: contain;
      @include screenMD {
        width: 65vw;
        height: 43.75vw;
        margin: 0 auto;
      }
    }
    &__tank {
      width: 17.5vw;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      @include screenMD {
        width: 34.24vw;
      }
    }
    &__msg {
      position: absolute;
      background-repeat: no-repeat;
      background-size: contain;
      @include flexCenter;
      > div {
        font-size: 0.36rem;
        line-height: 0.42rem;
        color: $secondary;
      }
      @keyframes msgZoomIn {
        from {
          transform: scale(0.5);
        }
        to {
          transform: scale(1);
        }
      }
      &--1 {
        width: 20.31vw;
        height: 6.1vw;
        top: -5.78vw;
        left: 26.71vw;
        background-image: url('@/assets/img/trouble_1_msg.png');
        > div {
          margin-bottom: 14px;
          @include animateTyping(2, true);
        }
        @include screenMD {
          width: 39.8vw;
          height: 11.94vw;
          top: -11.4vw;
          left: 41.28vw;
        }
      }
      &--2 {
        width: 18.54vw;
        height: 10.59vw;
        top: -3.85vw;
        left: -2.83vw;
        background-image: url('@/assets/img/trouble_2_msg.png');
        animation: 1.5s msgZoomIn 1.5s ease;
        > div {
          @include animateTyping(2, true);
        }
        @include screenMD {
          width: 28.11vw;
          height: 16.06vw;
          left: 8vw;
          top: -8vw;
        }
      }
    }
    &__title {
      @include textStroke;
      font-size: 0.36rem;
      line-height: 0.42rem;
      position: absolute;
      white-space: nowrap;
      @include screenMD {
        height: 28vw;
        text-align: center;
        margin-top: 8vw;
        @include flexCenter;
      }
      &--1 {
        top: 43.86%;
        right: -40%;
        @include screenMD {
          position: relative;
          top: 0;
          right: 0;
        }
      }
      &--2 {
        top: 57.72%;
        left: -40%;
        @include screenMD {
          position: relative;
          top: 50vw;
          left: 0;
        }
      }
      &--3{
        top: 69.12%;
        right: -40%;
        @include screenMD {
          position: relative;
          top: 50vw;
          left: 0;
        }
      }
    }
    &__soldier-wrap {
      width: 100%;
      height: 32.01vw;
      overflow: hidden;
      position: absolute;
      bottom: 0;
      @include screenMD {
        height: 62.6vw;
      }
    }
    &__soldier {
      width: 33.18vw;
      height: 32.01vw;
      position: absolute;
      bottom: 0;
      right: 12.24%;
      animation: 1s soldierMove 0.5s ease;
      @keyframes soldierMove {
        from {
          transform: translate(40%, 30%);
        }
        to {
          transform: translate(0%, 0%);
        }
      }
      @include screenMD {
        width: 64.88vw;
        height: 62.6vw;
      }
    }
    &__tree {
      width: 36.82vw;
      position: absolute;
      left: 50%;
      bottom: 0;
      transform: translateX(-50%);
      animation: 1.5s moveUp 0.5s ease;
      @include screenMD {
        width: 72.27vw;
        height: 67.84vw;
      }
    }
    &__soldier-back {
      width: 13.39vw;
      position: absolute;
      left: 32.35%;
      bottom: 0;
      animation: 1s moveUp 1s ease;
      @include screenMD {
        width: 26.3vw;
        height: 24.09vw;
      }
    }
    @keyframes moveUp {
      from {
        transform: translate(-50%, 30%);
      }
      to {
        transform: translate(-50%, 0%);
      }
    }
  }
</style>
