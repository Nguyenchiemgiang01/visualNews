
<template>
  <div class="layout">
    <Header />
    <div class="primary-content">

      <div class="content-wrapper">



        <div class="content" style="padding-right: 20px;">
          <div class="main-title">
            <h2 class="catagory-post">Advertisting</h2>
            <strong class="note">A simple description for this category</strong>
          </div>
          <div class="post" v-for="post in posts" :key="post.id">
            <PostDetail 
              :title="post.title"
              :image="post.image"
              :category="post.category" 
              :author="post.author"
              :day="post.day"
              :content="post.content" />
            </div>
          
         

          <div class="navigation">
            <div class="page-buttons">
              <a href="#">1</a>
              <a href="#">2</a>
            </div>
            <a href="#" class="next-button">Next</a>
          </div>
        </div>



        <div class="follow" style="margin-left: 10px;">
          <form class="search-form" action="" method="">
            <input style="background-color:#f1f1f1;width: 260px;padding: 7px 15px;height: 36px;" type="text" name="query"
              placeholder="Search for">
            <button style="background-color: rgb(16, 164, 218); width:36px;height:  36px;" type="submit">
              <svg style="margin-left: 10px;"
                xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-search"
                viewBox="0 0 16 16">
                <path
                  d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z" />
              </svg>
            </button>
          </form>


          <img style="width: 302px; height: 251px;"
            src="https://demo.wpenjoy.com/visualnews-pro/wp-content/themes/visualnews-pro/assets/images/300x250.png"
            alt="Post Image">

          <Follow />
          <Categoryname />
          <Fashion maintitle="RECENT POSTS" />
          <Tag style="margin-top: 120px;" />

        </div>

      </div>



    </div>


    <Footer style="margin-top: 50px;" />
  </div>
</template>
<script>

import PostDetail from '../components/typepost/postdetail.vue'
import Header from '../layout/Header';
import Content from '../components/content/Content.vue';
import Follow from '../components/follow/Follow.vue';
import Fashion from '../components/follow/Fashion.vue';
import Business from '../components/business/index.vue';
import Categoryname from '../components/typepost/catagoryname.vue';
import Tag from '../components/tag/tag.vue'

import Footer from "../layout/Footer"

export default {
  data() {
    return {
      posts: [
        {
          id: 1,
          title:'Reddit communities go private to protest pricing plan for apps',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
          image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/social-768x512.jpg',
          category: 'FASHION',
          author:'John Doe',
          day:'June 15, 2023',

        },
        {
          id: 2,
          title:'9 Ways to Engage Your Customers With Instagram Highlights',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
          image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/ins-768x512.jpg',
          category: 'ADVERTISING',
          author:'John Doe',
          day:'April 23, 2021',
        },
        {
          id: 3,
          title:'The 10-Step Guide to Creating a Profitable AdWords Campaign',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
          image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/google-768x512.jpg',
          category: 'Advertising',
          author:'John Doe',
          day:'April 23, 2021',
        },
        {
          id: 4,
          title:'Best Business Process Management Software',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
          image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/facebook.jpg',
          category: 'Advertising',
          author:'John Doe',
          day:'April 23, 2021',
        },
        {
          id: 5,
          title:'How to Use Amazon Attribution For Ad Campaigns',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
          image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2021/04/family-bathroom-768x512.jpeg',
          category: 'Advertising',
          author:'John Doe',
          day:'April 23, 2021',
        },
        {
          id: 6,
          title:'How to Use Amazon Attribution For Ad Campaigns',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
          image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/facebook.jpg',
          category: 'Advertising',
          author:'John Doe',
          day:'April 23, 2021',
        },
      ]
    };
  },

  components: {
    Header,
    Content,
    Follow,
    Business,
    PostDetail,
    Categoryname,
    Fashion,
    Tag,
    Footer

  }
}
</script>

<style scoped>
@media (min-width: 1200px) {
  .catagory-post {
    margin-top: 20px;
    font-weight: bolder;

  }

  .main-title {
    border-bottom: 2px solid #efecec;
  }

  .main-title>strong::before {
    content: "";
    position: absolute;
    width: 25px;
    height: 4px;
    background-color: #3780f5;
    margin-top: 36px;
  }

  .note {
    margin-top: 5px;
    margin-bottom: 10px;
    font-weight: lighter;
    font-size: small;
  }


  .follow {
    margin-left: auto;
  }

  .content-wrapper {
    margin: 0px 139.60px;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;

  }

  .navigation {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;


  }

  .page-buttons {
    display: flex;
    gap: 10px;
  }

  .page-buttons a {
    padding: 5px 10px;
    text-decoration: none;
    color: #0a0707;
    border: 1px solid #ccc;

    background-color: #52a6e2;
  }

  .navigation .next-button {
    background-color: #d4dae0;
    color: #171515;
    padding: 5px 10px;
    border: none;

  }

  .search-form {

    width: 302px;
    height: 70px;
    top: 100%;
    right: 0;
    margin-top: 12px;
    margin-bottom: 10px;

    background-color: #ffffff;

  }







}

@media (max-width: 760px) {
  .layout {
    flex-direction: column;
    width: 100%;

  }

  .service,
  .primary-content {
    margin: 0px 5px;
  }

}</style>
