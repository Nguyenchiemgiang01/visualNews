<template>
    <div class="main-content">
        <div class="follow">
                <strong>CATAGORY NAME</strong>
        </div>

        <div class="list-post">
            <ul class="post-tag">
                <li class="post" v-for="post in posts" :key="post.id">
                    <NuxtLink class="nuxt-link" to="#">
                        <div class="poster">
                            <img :src="post.image" alt="image">
                            <div class="info">
                             
                                <span class="title">
                                    <NuxtLink  class="post-title" :to="{path:'/postdetail/fashion',query:{title:post.title,category:post.category,image:post.image,author:post.author,day:post.day}  }">{{ post.title }}</NuxtLink>
                                </span>
                            </div>
                        </div>
                    </NuxtLink>
                </li>
            </ul>

        </div>

    </div>
</template>
<script>
import PostCategory from "../../components/post/PostCatagory.vue"

export default {
    data() {
        return {
            posts: [
             {
                 id: 1,
                 title: 'Why Apple Vision Pro’s $3,499 Price Makes More Sense Than You Think',
                 image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/solar-panels_EFYB8VJXNT-768x512.jpg',
                 category: 'TECHNOLOGY',
                 author:'John Doe',
                 day:'June 15, 2023'

             },
             {
                 id: 2,
                 title: 'The 6 biggest iOS 17 features that Apple stole from Android Digital Trends',
                 image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/apple-768x513.jpg',
                 category: 'ADVERTISTING',
                 author:'John Doe',
                 day:'June 15, 2023'
             },
             {
                 id: 3,
                 title: '9 Ways to Engage Your Customers With Instagram Highlights',
                 image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/ins-768x512.jpg',
                 category: 'TECHNOLOGY',
                 author:'John Doe',
                  day:'June 15, 2023'
             },
         ]
        };
    },
    components: { PostCategory }
}
</script>

<style scoped>
   .follow {
        font-size: 14px;
        text-decoration: none;
        /* Loại bỏ gạch chân mặc định */
        position: relative;
        border-bottom: 2px solid #e7eaec;
        /* Tạo đoạn gạch dưới ngắn */
        padding-bottom: 5px;
        margin-bottom: 10px;
    }

    .follow>strong::before {
        content: "";
        position: absolute;
        bottom: -2px;
        left: 0;
        width: 25px;
        height: 4px;
        background-color: #3780f5;
    }
    
    .post {
        margin-top: 20px;
        text-decoration: none;
        /* Loại bỏ gạch chân mặc định */
        position: relative;
        border-bottom: 2px solid #e7eaec;
        /* Tạo đoạn gạch dưới ngắn */
        padding-bottom: 25px;
        margin-bottom: 20px;
    }
.main-content {
    /* Các thuộc tính CSS cho main-post */
    display: flex;
    margin-top: 25px;
    margin-right: 4%;
    flex-direction: column;
    width: 302px;
}



.post-tag {
    list-style: none;
    padding: 0;
    margin: 0;
}


.poster>img {

    width: 302px;
    /* Kích thước của ảnh */
    height: 120px;

}
.title {
    margin-bottom: 10px;
    margin: 0;
    font-size: 16px;
    /* Kích thước nhỏ hơn */
    font-weight: bold;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    /* Số dòng tối đa */
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
}
</style>