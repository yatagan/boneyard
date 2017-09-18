<template>
  <div class="chat_item_wrap">
    <div class="chat_hash">
      #{{ name }}
    </div>
    <div class="chat_detail_wrap">
      <div class="chat_view_num">
        <img src="/images/DesktopImages/green-ball.png" alt="green ball" />
        <span>{{ usersComma }}</span>
      </div>
      <div class="chat_join_button">
        <button class="button is-small join_button_grey">Join</button>
      </div>
    </div>
  </div>
</template>

<script>
  module.exports = {
    props: [
      'name',
      'usersNumber'
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
.trending_chat {

  .chat_item_wrap {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 50px;
    border-top: 1px solid $bar-lightgrey;
    padding-left: 1rem;
    padding-right: 1rem;
    .chat_hash {
      font-size: 1.25rem;
      font-weight: 700;
    }
  }
  .chat_item_wrap:last-child {
    border-bottom: 1px solid $bar-lightgrey;
  }
  .chat_detail_wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 45%;
    .chat_view_num {
      display: flex;
      align-items: center;
      span {
        font-size: 1.25rem;
        font-weight: 500;
        padding-left: 0.5rem;
      }
    }
  }
  .join_button_grey {
    background-color: $button-grey;
    color: $button-grey-text;
    width: 50px;
    border-radius: 5px;
    border: 0;
    padding-top: 0.25rem;
    padding-bottom: 0.25rem;
    text-align: center;
    font-weight: 500;
  }
}
</style>
