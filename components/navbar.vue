<template>
  <nav class="navbar">
    <div class="left">
      <ul>
        <li>
          <img src="@/assets/img/logo.svg" />
        </li>
        <li>關卡資訊</li>
        <a href="https://hackmd.io/ofJD4K7iSI65V19zxC7d0w" target="_blank">
          <li>攻略資源</li>
        </a>
        <a href="https://2022.thef2e.com/jobs" target="_blank">
          <li>求職專區</li>
        </a>
      </ul>
    </div>
    <div class="right">
      <ul>
        <a href="https://2022.thef2e.com/signup" target="_blank">
          <li>
            <button>
              <span>註冊報名</span>
            </button>
          </li>
        </a>
        <a href="https://2022.thef2e.com/login" target="_blank">
          <li>
            <button>
              <span>登入</span>
            </button>
          </li>
        </a>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>

<style lang="scss">
  .navbar {
    background-color: $primary;
    padding: 10px 12.5%; // container
    @include flexCenterH;
    justify-content: flex-end;
    @include screenLG {
      padding: 10px 2.43%; // container
    }
    @include screenMD {
      padding: 10px 3.26%; // container
      justify-content: space-between;
    }
    @include screenSM {

    }
    ul {
      @include flexCenterH;
    }
    li {
      cursor: pointer;
      color: $secondary;
      font-size: 16px;
      line-height: 19px;
      &:hover {
        color: $white;
      }
    }
    .left {
      li {
        margin-right: 30px;
      }
    }
    .right {
      button {
        @include buttonSM;
      }
      li {
        &:first-child {
          margin-right: 10px;
        }
      }
    }
  }
</style>
