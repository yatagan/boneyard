<template>
  <div class="top-nav full-width">
    <div class="nav-content">
      <div class="nav-item-group">
        <div class="nav-item-wrap">
          <div class="nav-icon">

            <h4><i class="fa fa-fire" aria-hidden="true"></i></h4>

            <!--<img src="/" alt="fire" />-->
          </div>
          <div class="nav-text">
            <h4>TRENDING</h4>
          </div>
        </div>
        <div class="nav-item-wrap">
          <div class="nav-icon">
            <h4><i class="fa fa-star" aria-hidden="true"></i></h4>
          </div>
          <div class="nav-text">
            <h4>MOST POPULAR</h4>
          </div>
        </div>
        <div class="nav-item-wrap">
          <div class="nav-icon">
            <h4><i class="fa fa-heart" aria-hidden="true"></i></h4>
          </div>
          <div class="nav-text">
            <h4>MOST LOVED</h4>
          </div>
        </div>
        <div class="nav-item-wrap">
          <div class="nav-icon">
            <h4><i class="fa fa-gift" aria-hidden="true"></i></h4>
          </div>
          <div class="nav-text">
            <h4>LATEST</h4>
          </div>
        </div>
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
          .nav-text {
            margin-left: 0.5rem;
            margin-right: 1rem;
          }
        }
      }
    }
  }
</style>
