<template>
  <div class="stage">
    <div ref="stageWrap" class="stage__wrap">
      <div class="stage__view">
        <img class="stage__bg" src="@/assets/img/stage_1.png" />
        <div class="stage__content">
          <div class="stage__week">WEEK 1</div>
          <div class="stage__title">The F2E 活動網站設計</div>
          <div class="stage__subtitle">視差滾動</div>
          <div class="stage__tag">#版塊設計</div>
          <div class="stage__flag-wrap">
            <div class="stage__line"></div>
            <div class="stage__flag"></div>
          </div>
          <button>查看關卡細節</button>
        </div>
      </div>
      <div class="stage__view">
        <img class="stage__bg" src="@/assets/img/stage_2.png" />
        <div class="stage__content">
          <div class="stage__week">WEEK 2</div>
          <div class="stage__title">今晚，我想來點點簽</div>
          <div class="stage__subtitle">canvas</div>
          <div class="stage__tag">#凱鈿行動科技</div>
          <div class="stage__flag-wrap">
            <div class="stage__flag"></div>
          </div>
          <button>查看關卡細節</button>
        </div>
      </div>
      <div class="stage__view">
        <img class="stage__bg" src="@/assets/img/stage_3.png" />
        <div class="stage__content">
          <div class="stage__week">WEEK 3</div>
          <div class="stage__title">Scrum 新手村</div>
          <div class="stage__subtitle">JS draggable</div>
          <div class="stage__tag">#鈦坦科技</div>
          <div class="stage__flag-wrap">
            <div class="stage__flag"></div>
          </div>
          <button>查看關卡細節</button>
        </div>
      </div>
      <div class="stage__tank-wrap">
        <img
          class="stage__tank"
          src="@/assets/img/tank_1.gif"
          :style="`transform: translateX(${tankPosition}px)`"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StageView',

  data() {
    return {
      tankPosition: 0,
    }
  },

  mounted() {
    const element = this.$refs.stageWrap;
    element.addEventListener('scroll', this.scrollHandler);
  },

  destroyed() {
    const element = this.$refs.stageWrap;
    element.removeEventListener('scroll', this.scrollHandler);
  },

  methods: {
    scrollHandler() {
      this.tankPosition = this.$refs.stageWrap.scrollLeft;

    },
  },
}
</script>

<style lang="scss">
  .stage {
    &__wrap {
      display: flex;
      overflow-x: scroll;
    }
    &__view {
      width: 100vw;
      min-height: 100vh;
      flex-shrink: 0;
      &:nth-child(1) {
        background-color: $primary;
      }
      &:nth-child(2) {
        background-color: $blue-bg;
        .stage__week {
          color: $blue;
        }
      }
      &:nth-child(3) {
        background-color: $green-bg;
        .stage__week {
          color: $green;
        }
      }
    }
    &__bg {
      max-height: 100vh;
      max-width: 100vw;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
    }
    &__content {
      position: absolute;
      z-index: 1;
      top: 50%;
      left: 50%;
      padding-top: 5%;
      transform: translate(-50%, -50%);
      text-align: center;
      width: 100%;
    }
    &__week {
      font-size: 0.52rem;
      line-height: 0.61rem;
      color: $tertiary;
      margin-bottom: 8px;
    }
    &__title {
      font-size: 0.72rem;
      line-height: 0.84rem;
      margin-bottom: 47px;
    }
    &__subtitle,
    &__tag {
      font-size: 0.36rem;
      line-height: 0.42rem;
      margin-bottom: 17px;
    }
    &__tag {
      margin-bottom: 42px;
    }
    &__flag-wrap {
      height: 229px;
      margin: 0 auto;
      z-index: 1;
    }
    &__line {
      height: 1px;
      width: 200vw;
      border-bottom: 5px dashed rgba(255, 255, 255, 0.5);
      position: absolute;
      bottom: 22%;
      left: 53.75%;
    }
    &__tank-wrap {
      position: absolute;
      bottom: 14vw;
      left: 50%;
      transform: translateX(-50%);
      z-index: 1;
      @include screenMD {
        bottom: 30vw;
      }
      @include screenSM {
        bottom: 45vw;
        margin-left: -3vw;
      }
    }
    &__tank {
      width: calc(207px / 2);
      height: calc(83px / 2);
      position: absolute;
      top: 50%;
      left: -2vw;
      transition: 1s all ease;
      z-index: 1;
    }
    &__flag {
      width: 140.8px;
      height: 229px;
      background-image: url("@/assets/img/flag_sprite.png");
      background-repeat: no-repeat;
      position: absolute;
      left: 50%;
      transform: translateX(-50%) scale(calc(140.8 / 1920 * 10));
      animation: spriteFlag 1s steps(4) infinite;
      @keyframes spriteFlag {
        from { background-position: 0px; }
        to { background-position: -563.2px; }
      }
    }
    button {
      @include buttonLG;
      margin: 0 auto;
    }
  }
</style>
