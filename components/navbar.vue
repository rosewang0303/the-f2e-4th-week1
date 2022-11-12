<template>
  <nav class="navbar container">
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
            <button>註冊報名</button>
          </li>
        </a>
        <a href="https://2022.thef2e.com/login" target="_blank">
          <li>
            <button>登入</button>
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

<style lang="scss" scoped>
  .navbar {
    background-color: $primary;
    @include flexCenterH;
    justify-content: flex-end;
    // container
    padding-top: 10px;
    padding-bottom: 10px;
    @include screenMD {
      justify-content: space-between;
    }
    @include screenSM {
      // TODO
    }
    ul {
      @include flexCenterH;
    }
    li {
      cursor: pointer;
      color: $secondary;
      font-size: 0.16rem;
      line-height: 0.19rem;
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
      a {
        &:first-child {
          margin-right: 10px;
        }
      }
    }
  }
</style>
