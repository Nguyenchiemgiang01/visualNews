<template>
    <div class="main-content">
        <img class="mainimage" :src="post.image" alt="image content">
        <NuxtLink style="font-weight: bolder;" class="post-title" :to="{path:'/postdetail/fashion',query:{title:post.title,category:post.category,image:post.image,author:post.author,day:post.day}  }">{{ post.title }}</NuxtLink>

    </div>
</template>

<script>
export default {
    data() {
        return {
            post:
            {
                title: 'TikTok’s latest trending beauty filter returns users to their younger selves',
                image: 'https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/girl-768x512.jpg',
                category: 'LIFESTYLE',
                 author:'John Doe',
                 day:'June 15, 2023',
          
            }

        };
    }
}
</script>
<style>
@media (min-width: 1200px) {

    .mainimage {
        width: 500px;
        height: 300px;

    }

    .main-title {
      
        color: black;
        font-size: 22.48px;
        font-weight: bold;
    }

}

@media (max-width:760px) {
    .main-content {
        margin-bottom: 40px;
    }

    .main-title {
        font-size: 18px;
        color: black;
        font-weight: bold;
        margin-top: 15px;
    }
}
</style>