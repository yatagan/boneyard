<template>
  <section class="container has-text-centered">
    <div class="main_content">
      <h1 class="main-title">
        Chatyard
      </h1>
      <h2 class="subtext">
        Chat with amazing people about any <strong>#topics</strong>
      </h2>
      <div class="disclaimer">
        <p>CREATE A CHAT GROUP OR JOIN</p>
      </div>
      <div class="input_wrap">
        <input class="input_name is-large" type="text" placeholder="Add a name" />
      </div>
      <button class="button is-medium start_button">GET STARTED</button>
    </div>
    <div class="featured_chat">
      <h2><strong>Featured</strong> Chatrooms</h2>

      <div class="columns is-gapless">
        <div class="column is-4">
          <div class="content_wrap">
            <div class="image">
              <img src="/images/football-american-game-runner.jpg" alt="football" />
            </div>
            <div class="detail_info_wrap">
              <div class="hashtag">
                <span>#Sports</span>
              </div>
              <div class="view_num">
                <span>27,000</span>
              </div>
              <div class="join_button">
                <button class="button is-outlined is-small">Join</button>
              </div>
            </div>
          </div>
        </div>
        <div class="column is-4">
          <div class="content_wrap">
            <div class="image">
              <img src="/images/Zoro-The-Drummer.jpg" alt="drummer" />
            </div>
            <div class="detail_info_wrap">
              <div class="hashtag">
                <span>#Music</span>
              </div>
              <div class="view_num">
                <span>15,700</span>
              </div>
              <div class="join_button">
                <button class="button is-outlined is-small">Join</button>
              </div>
            </div>
          </div>
        </div>
        <div class="column is-4">
          <div class="content_wrap">
            <div class="image">
              <img src="/images/download.jpg" alt="microchip" />
            </div>
            <div class="detail_info_wrap">
              <div class="hashtag">
                <span>#Electronics</span>
              </div>
              <div class="view_num">
                <span>27,000</span>
              </div>
              <div class="join_button">
                <button class="button is-outlined is-small">Join</button>
              </div>
            </div>
          </div>
        </div>
      </div>

      <button class="view_all_button">
        VIEW ALL CHATROOMS
      </button>
    </div>

    <div class="trending_chat">
      <h2><strong>Trending</strong> Chatrooms</h2>
      <div class="red_underline">

      </div>

      <div class="columns">
        <div class="column is-6">
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #FriendsForever
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                27,246
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>

          </div>
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #SoccerLovers
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                12,888
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>

          </div>
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #TravelLovers
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                33,465
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>

          </div>
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #Singles
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                12,444
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>
          </div>

        </div>
        <div class="column is-6">
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #BieberFans
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                47,246
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>
          </div>
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #TrumpFever
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                184,888
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>
          </div>
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #FriendsFanClub
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                1,000,465
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>
          </div>
          <div class="chat_item_wrap">
            <div class="chat_hash">
              #WWESummerSlam
            </div>
            <div class="chat_detail_wrap">
              <div class="chat_view_num">
                4,544
              </div>
              <div class="chat_join_button">
                <button class="button is-small join_button_grey">Join</button>
              </div>
            </div>
          </div>
        </div>
      </div>

      <button class="view_all_trending">
        VIEW ALL TRENDING
      </button>
    </div>
  </section>
</template>
<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>
<style lang="scss" rel="stylesheet/scss" scoped >
  @import "~assets/css/variables.scss";

  ::-webkit-input-placeholder { /* Chrome/Opera/Safari */
    text-align: center;
    font-size: 1.5rem;
    font-weight: 300;
  }
  ::-moz-placeholder { /* Firefox 19+ */
    text-align: center;
    font-size: 1.5rem;
    font-weight: 300;
  }
  :-ms-input-placeholder { /* IE 10+ */
    text-align: center;
    font-size: 1.5rem;
    font-weight: 300;
  }
  :-moz-placeholder { /* Firefox 18- */
    text-align: center;
    font-size: 1.5rem;
    font-weight: 300;
  }

  h1 {
    font-size: 51px;
    font-weight: 500;
  }

  h2 {
    color: $black;
  }

  .container {
    padding-bottom: 5rem;
  }

  .main_content {
    padding-top: 4rem;
  }

  .main-title {
    margin-top: 3.5rem;
    color: $red;
  }

  .subtext {
    margin-top: 1rem;
    font-size: 2rem;
    font-weight: 300;
  }
  .disclaimer {
    margin-top: 5rem;
    font-size: 12px;
  }

  .input_wrap {

    width: 55%;
    margin: 0 auto;
    margin-top: 2rem;
    .input_name {
      width: 100%;
      height: 50px;
      border-top: 0px;
      border-left: 0px;
      border-right: 0px;
    }
  }
  .start_button {
    margin-top: 2rem;
    font-size: 1rem;
    background-color: $red;
    color: white;
    border-radius: 100px;
    padding-left: 3.5rem;
    padding-right: 3.5rem;
    height: $main-button-height;
  }

  .featured_chat {
    margin-top: 10rem;
    h2 {
      font-size: 2.25rem;
      margin-bottom: 1rem;
    }
    .content_wrap {
      .image {
        min-height: 255px;
        background-color: black;
      }
    }
    .detail_info_wrap {
      height: 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;

      .join_button {
        .button {
          border-radius: 10px;
        }

      }
    }
    .view_all_button {
      margin-top: 2rem;
      height: 40px;
      padding-left: 2.5rem;
      padding-right: 2.5rem;
      color: white;
      background-color: $red;
      border-radius: 100px;
      border: 0;
      font-size: 1rem;
    }
  }
  .trending_chat {
    margin-top: 10rem;
    .columns {
      .column {
        padding-left: 4rem;
        padding-right: 4rem;
      }
    }
    h2 {
      font-size: 2.25rem;
      margin-bottom: 1rem;
    }
    .red_underline {
      height: 4px;
      border-top: 2px solid $red;
      width: 15%;
      margin: 0 auto;
      margin-bottom: 3rem;
    }
    .chat_item_wrap {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 50px;
      border-top: 1px solid $bar-lightgrey;
      padding-left: 1rem;
      padding-right: 1rem;
    }
    .chat_item_wrap:last-child {
      border-bottom: 1px solid $bar-lightgrey;
    }
    .chat_detail_wrap {
      display: flex;
    }
    .chat_view_num {
      width: 75px;
      display: flex;
      flex: 0 0 auto;
    }
    .chat_join_button {
      display: flex;
      flex: 0 0 auto;
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
    }
    .view_all_trending {
      margin-top: 2rem;
      height: 40px;
      padding-left: 2.5rem;
      padding-right: 2.5rem;
      color: white;
      background-color: #ff585b;
      border-radius: 100px;
      border: 0;
      font-size: 1rem;
    }
  }

</style>
