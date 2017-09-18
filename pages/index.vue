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
        <div v-for="item in featured" class="column is-4">
          <featured-chat-item
            :key="item.id"
            :name="item.name"
            :users-number="item.usersNumber"
            :image="item.image"></featured-chat-item>
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

          <trending-chat-item
            v-for="item in trendingLeft"
            :key="item.id"
            :name="item.name"
            :users-number="item.usersNumber"></trending-chat-item>

        </div>
        <div class="column is-6">

          <trending-chat-item
            v-for="item in trendingRight"
            :key="item.id"
            :name="item.name"
            :users-number="item.usersNumber"></trending-chat-item>

        </div>
      </div>

      <button class="view_all_trending">
        VIEW ALL TRENDING
      </button>
    </div>

    <div class="social_media">
      <div class="columns social_columns">
        <div class="column about">
          <h3>ABOUT CHATYARD</h3>
          <a href="">ABOUT US</a>
          <a href="">CAREERS</a>
          <a href="">POLICIES</a>
          <a href="">HELP</a>
        </div>
        <div class="column about">
          <h3>ABOUT CHATYARD</h3>
          <a href="">ABOUT US</a>
          <a href="">CAREERS</a>
          <a href="">POLICIES</a>
          <a href="">HELP</a>
        </div>
        <div class="column about">
          <h3>ABOUT CHATYARD</h3>
          <a href="">ABOUT US</a>
          <a href="">CAREERS</a>
          <a href="">POLICIES</a>
          <a href="">HELP</a>
        </div>
        <div class="column is-5 social_network">
          <div class="social_wrap">
            <h3>FOLLOW US</h3>
            <div class="social_icon_wrap">
              <img src="/images/DesktopImages/social-fb.png" alt="facebook" />
              <img src="/images/DesktopImages/social-pinterest.png" alt="pinterest" />
              <img src="/images/DesktopImages/social-twitter.png" alt="twitter" />
            </div>
          </div>

        </div>

      </div>
    </div>
  </section>
</template>
<script>
import _ from 'lodash'
import axios from 'axios'

import Logo from '~/components/Logo.vue'
//import socket from '~/components/socket.js'

import FeaturedChatItem from '~/components/FeaturedChatItem.vue'
import TrendingChatItem from '~/components/TrendingChatItem.vue'


export default {
  components: {
    Logo,
    FeaturedChatItem,
    TrendingChatItem
  },
  data: function () {
    return {
      chatrooms: [],
      trending: []
    }
  },
  computed: {
    featured: function () {
      let num = 3;
      return _.take(this.chatrooms, num);
    },
    trendingLeft: function () {
      let length = this.trending.length;
      let numLeft = _.ceil(length / 2);
      return _.take(this.trending, numLeft);
    },
    trendingRight: function () {
      let length = this.trending.length;
      let numLeft = _.ceil(length / 2);
      let nubRight = length - numLeft;
      return _.takeRight(this.trending, nubRight);
    }
  },
  beforeMount: function () {
    this.loadChatrooms();
  },
  methods: {
    loadChatrooms: function () {
      var vm = this;
      axios.get('api/chatrooms')
        .then(function(resp) {
          if (typeof resp.data === 'object') {
            vm.chatrooms = resp.data;
          }
          else {
            throw 'Invalid response';
          }
        })
        .catch(function (error) {
          vm.loadDummyChatrooms();
          console.warn('Loaded dummy data');
        });
    },
    loadDummyChatrooms: function () {
      this.chatrooms = [
        {name: 'Sports', usersNumber: 27000, image: '/images/football-american-game-runner.jpg'},
        {name: 'Music', usersNumber: 15700, image: '/images/Zoro-The-Drummer.jpg'},
        {name: 'Electronics', usersNumber: 27000, image: '/images/download.jpg'},
      ];
      this.trending = [
        {name: 'FriendsForever', usersNumber: 27246},
        {name: 'SoccerLovers', usersNumber: 12888},
        {name: 'TravelLovers', usersNumber: 33465},
        {name: 'Singles', usersNumber: 12444},

        {name: 'BieberFans', usersNumber: 46246},
        {name: 'TrumpFever', usersNumber: 184754},
        {name: 'FriendsFanClub', usersNumber: 1000465},
        {name: 'WWESummerSlam', usersNumber: 4544},
      ];
    }
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
    padding-left: 1rem;
    padding-right: 1rem;
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
      text-align: center;
      font-size: 1.5rem;
      width: 100%;
      height: 50px;
      border-top: 0px;
      border-left: 0px;
      border-right: 0px;
    }
  }
  .start_button {
    margin-top: 2rem;
    font-size: 1.25rem;
    background-color: $red;
    color: white;
    border-radius: 100px;
    border: 0;
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
    .view_all_button {
      margin-top: 2rem;
      height: $main-button-height;
      padding-left: 3rem;
      padding-right: 3rem;
      color: white;
      background-color: $red;
      border-radius: 100px;
      border: 0;
      font-size: 1.25rem;
      cursor: pointer;
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
    .view_all_trending {
      margin-top: 2rem;
      width: 340px;
      height: $main-button-height;
      padding-left: 3rem;
      padding-right: 3rem;
      color: white;
      background-color: #ff585b;
      border-radius: 100px;
      border: 0;
      font-size: 1.25rem;
      cursor: pointer;
    }
  }

  .social_media {
    margin-top: 10rem;
    .social_columns {
      align-items: flex-start;
      .about {
        text-align: left;
        h3 {
          font-size: 1rem;
          font-weight: 500;
        }
        a {
          display: block;
          font-size: 0.85rem;
          color: $black;
          line-height: 2;
        }
      }
      .social_network {
        .social_wrap {
          width: 90%;
          margin: 0 auto;
          text-align: left;
          h3 {
            font-size: 1rem;
            font-weight: 500;
          }
          .social_icon_wrap {
            margin-top: 1rem;
            img {
              margin-right: 1.5rem;
            }
          }
        }
      }
    }
  }

</style>
