<template>
  <div class="content_wrap">
    <div class="image">
      <img v-bind:src="image" alt="football" />
    </div>
    <div class="detail_info_wrap">
      <div class="hashtag">
        <span>#{{ name }}</span>
      </div>
      <div class="view_num join_button">
        <div class="view_count">
          <img src="/images/DesktopImages/green-ball.png" alt="green ball" />
          <span>{{ usersComma }}</span>
        </div>
        <button class="button join_button_grey is-outlined is-small">Join</button>
      </div>
    </div>
  </div>
</template>

<script>
  module.exports = {
    props: [
      'name',
      'usersNumber',
      'image'
    ],
    computed: {
      usersComma: function () {
        return this.usersNumber.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
      }
    }
  }
</script>

<style lang="scss" rel="stylesheet/scss" scoped >

@import "~assets/css/variables.scss";

.featured_chat {

  .content_wrap {
    .image {
      height: 250px;
      background-color: black;
      img {
        height: 100%
      }
    }
  }
  .detail_info_wrap {
    height: 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-left: 1rem;
    padding-right: 1rem;
    .hashtag {
      span {
        font-size: 1.25rem;
        font-weight: 700;

      }
    }
    .view_num {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 50%;
      .view_count {
        display: flex;
        align-items: center;
        span {
          font-size: 1.25rem;
          font-weight: 500;
          padding-left: 0.5rem;
        }
      }
    }

    .join_button {
      .join_button_grey {
        background-color: $button-grey;
        color: $button-grey-text;
        width: 50px;
        border-radius: 5px;
        border: 0;
        padding-top: 0.25rem;
        padding-bottom: 0.25rem;
        text-align: center;
      }

    }
  }
}
</style>
