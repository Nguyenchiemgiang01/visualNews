<template>
    <div class="business">
        <div class="head">
            <div class="container">
                <div class="row  tab-business align-items-center">
                    <div class="col ">
                        <NuxtLink to="#">
                            <h2 class="bus link">BUSINESS</h2>
                        </NuxtLink>

                    </div>
                    <div class="col ">
                        <NuxtLink to="#">
                            <h2 class="sub-bus link">SUB CAT 1</h2>
                        </NuxtLink>
                    </div>
                    <div class="col ">
                        <NuxtLink to="#">
                            <h2 class="sub-bus link">SUB CAT 2</h2>
                        </NuxtLink>
                    </div>
                    <div class="col ">
                        <NuxtLink to="#">
                            <h2 class="sub-bus link">SUB CAT 3</h2>
                        </NuxtLink>
                    </div>
                    <div class="col ">
                        <NuxtLink to="#">
                            <h2 class="sub-bus link">SUB CAT 4</h2>
                        </NuxtLink>
                    </div>
                </div>
            </div>
        </div>
        <div class="posts">
            <div class="container">
                <div class="row">
                    <div class="col-md-4  custom-col" v-for="post in posts" :key="post.id">
                        <div class="post">
                            <img :src="post.image" alt="Post Image">
                            <div class="info">
                                <div class="post-category">
                                    <p>{{ post.category }}</p>
                                </div>
                                <NuxtLink  class="post-title" :to="{path:'/postdetail/fashion',query:{title:post.title,category:post.category,image:post.image,author:post.author,day:post.day}  }">{{ post.title }}</NuxtLink>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            posts: [
                {
                    id: 1,
                    title: 'The job market enters a new phase as the Great Resignation ends',
                    image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/saulo-mohana-768x511.jpg',
                    category: 'BUSINESS',
                    author:'John Doe',
                    day:'June 15, 2023',

                },
                {
                    id: 2,
                    title: 'Musk is no longer the CEO of Twitter. Linda Yaccarino officially starts in role',
                    image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/adem-ay-Tk9m_HP4rgQ-768x512.jpg',
                    category: 'BUSINESS',
                    author:'John Doe',
                    day:'June 15, 2023',
                },
                {
                    id: 3,
                    title: 'Deciding what to do when your employer changes the rules on remote work',
                    image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/jason-goodman-768x512.jpg',
                    category: 'BUSINESS',
                    author:'John Doe',
                    day:'June 15, 2023'
                },

            ]
        };
    },
}
</script>

<style scoped>
@media (max-width:760px) {
    .custom-col{
        padding: 0px 0px ;
    }
    .head {
        border-bottom: 1px solid #efeaea;
        margin-right: 40px;
    }

    .tab-business {

        width: 440px;
        height: 41px;
    }

    .tab-business {
        font-size: 14px;
        text-decoration: none;
        /* Loại bỏ gạch chân mặc định */
        position: relative;
        border-bottom: 2px solid #ffffff;
        /* Tạo đoạn gạch dưới ngắn */
        padding-bottom: 5px;

    }

    .tab-business::before {
        content: "";
        position: absolute;
        bottom: -2px;
        left: 0;
        width: 25px;
        height: 4px;
        background-color: #3780f5;
    }

    .tab-business>.col {

        padding: 0px;
    }

    .bus {
        font-size: 16px;
        margin-right: 10px;
        font-weight: bold;
        color: black;
    }

    .sub-bus {
        display: none;
    }
    .post {
        margin-top: 25px;
        margin-bottom: 20px;
        background-color: #ffffff;
    }
    .post-category p {
        margin-top: 10px;

        text-transform: uppercase;
        color: #cdc6c6;
        /* Màu nhạt */
        font-size: 0.8em;
        align-self: flex-start;
        margin-bottom: 5px;

    }

    .post-title {
        padding-right: 10px;
        font-size: 1em;
        /* Kích thước nhỏ hơn */
        font-weight: bold;
        display: -webkit-box;
        -webkit-line-clamp: 3;
        /* Số dòng tối đa */
        -webkit-box-orient: vertical;
        overflow: hidden;
        text-overflow: ellipsis;
    }

}
@media (min-width: 1200px) {

    .head {
        border-bottom: 1px solid #efeaea;
        margin-right: 40px;
    }

    .tab-business {

        width: 440px;
        height: 41px;
    }

    .tab-business {
        font-size: 14px;
        text-decoration: none;
        /* Loại bỏ gạch chân mặc định */
        position: relative;
        border-bottom: 2px solid #ffffff;
        /* Tạo đoạn gạch dưới ngắn */
        padding-bottom: 5px;

    }

    .tab-business::before {
        content: "";
        position: absolute;
        bottom: -2px;
        left: 0;
        width: 25px;
        height: 4px;
        background-color: #3780f5;
    }

    .tab-business>.col {

        padding: 0px;
    }

    .bus {
        font-size: 16px;
        margin-right: 10px;
        font-weight: bold;
        color: black;
    }

    .sub-bus {

        font-size: 13px;
        font-weight: bold;
        color: #b6b1b1;
    }

    .link :hover {
        text-decoration: none;
        color: black;
    }

    .post {
        margin-top: 25px;
        margin-bottom: 20px;
        background-color: #ffffff;
    }

    .custom-col {
        padding-left: 0;
        padding-right: 10px;
    }

    .post>img {
        width: 287px;
        height: 190px;
    }

    .post-category p {
        margin-top: 10px;

        text-transform: uppercase;
        color: #cdc6c6;
        /* Màu nhạt */
        font-size: 0.8em;
        align-self: flex-start;
        margin-bottom: 5px;

    }

    .post-title {
        padding-right: 10px;
        font-size: 1em;
        /* Kích thước nhỏ hơn */
        font-weight: bold;
        display: -webkit-box;
        -webkit-line-clamp: 3;
        /* Số dòng tối đa */
        -webkit-box-orient: vertical;
        overflow: hidden;
        text-overflow: ellipsis;
    }

}</style>