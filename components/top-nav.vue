<template>
  <div class="top-nav full-width">
    <div class="nav-content">
      <div class="nav-item-group">
        <a class="nav-item-wrap">
          <div class="nav-icon">
            <img src="/images/DesktopImages/chat-trending.png" alt="fire" />
          </div>
          <div class="nav-text">
            <h4>TRENDING</h4>
          </div>
        </a>
        <a class="nav-item-wrap">
          <div class="nav-icon">
            <img src="/images/DesktopImages/chat-mostpopular.png" alt="popular" />
          </div>
          <div class="nav-text">
            <h4>MOST POPULAR</h4>
          </div>
        </a>
        <a class="nav-item-wrap">
          <div class="nav-icon">
            <img src="/images/DesktopImages/chat-mostloved.png" alt="loved" />
          </div>
          <div class="nav-text">
            <h4>MOST LOVED</h4>
          </div>
        </a>
        <a class="nav-item-wrap">
          <div class="nav-icon">
            <img src="/images/DesktopImages/chat-latest.png" alt="latest" />
          </div>
          <div class="nav-text">
            <h4>LATEST</h4>
          </div>
        </a>
      </div>
      <div class="nav-right">
        <div class="login">
          <a ><h4>LOGIN / REGISTER</h4></a>
        </div>
      </div>

    </div>

  </div>
</template>
<script type="text/ecmascript-6">

  export default {
    components: {

    }
  }
</script>
<style lang="scss" rel="stylesheet/scss" scoped>
  @import "~assets/css/variables.scss";

  h4 {
    color: $black;
  }
  .top-nav {
    width: 100%;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid black;
    .nav-content {
      width: 1050px;
      margin: 0 auto;
      display: flex;
      padding-left: 1rem;
      padding-right: 1rem;
      .nav-item-group {
        display: flex;
        align-items: center;
        .nav-item-wrap {
          display: flex;
          align-items: center;
          .nav-text {
            margin-left: 0.25rem;
            margin-right: 1rem;
          }
        }
      }
      .nav-right {
        display: flex;
        align-items: center;
      }
    }
  }
</style>
