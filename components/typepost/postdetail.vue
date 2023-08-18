<template>
    <div class="post">
        <img :src="image" alt="Post Image">
        <div class="info">
            <div class="title-post">
                <NuxtLink   :to="{path:'/postdetail/fashion',query:{title:title,category:category,image:image,author:author,day:day}  }">{{ title }}</NuxtLink>
            </div>
            <div class="info-post">
                <p>{{category }}</p>
                <p> . By {{ author }}</p>
                <p>- {{ day }}</p>
            </div>
            <div class="content-post">{{ content }}</div>
           
        </div>
    </div>

</template>
<script>
export default {
props: {
    image: {
        type: String,
        default: "/fashion1.jpg",
    },
    category: {
        type: String,
        default: "TRAVEL"

    },

    title: {
        type: String,
        default: "The best smart glasses to buy now, according to experts asdasdasda",
    },
    author:{
        type:String,
        default:"John Doe"
    },
    day:{
        type:String,
        default:"April 23, 2021"
    },
    content:{
        type:String,
        default:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,"
    }
    
}
}
</script>
<style scoped>
@media (max-width:760px) {
    .post{
        display: block;
    }
.post>img {
width: 100%;
height: 190px;
}
.post-title {
margin:10px 20px;
padding-right: 10px;
font-size: 18px;
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

.post {
    margin-top: 25px;
    margin-bottom: 20px;
    height: 210px;
    padding-bottom: 10px;
    border-bottom: 2px solid #efecec;
    }
.title-post{
    font-weight: bolder;
    font-size: 24px;
}
.post>img {
width: 260x;
height: 173.663px;
margin-right: 10px;
}
.post {
    display: flex;
    align-items: flex-start;
}


.post .info {
    width: 70%; /* Adjust as needed */
    display: flex;
    flex-direction: column;
    margin-top: 2px
   
}

.info-post {
    display: flex;
    align-items: center;
    margin-top: 10px;
}

.info-post p {
    margin: 0; /* Remove default margin for <p> elements */
    margin-right: 1rem; /* Add spacing between info-post items */
    margin-top:2px
}
.content-post{
    margin-top: 10px;
    font-size: 16px;
}





}


</style>