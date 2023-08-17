<template>
    <div class="tag">
        <div class="tag-title">
            <strong>Tag</strong>
        </div>
        <p class="list-tag"  >
                <a style="font-size:13px;" v-for="tag in tags" :href="tag.href " >{{tag.title}}</a>
        </p>
    </div>
</template>
<style scoped>
.tag{
    width: 302px;
}
   .tag-title {
        font-size: 14px;
        text-decoration: none;
        /* Loại bỏ gạch chân mặc định */
        position: relative;
        border-bottom: 2px solid #e7eaec;
        /* Tạo đoạn gạch dưới ngắn */
        padding-bottom: 5px;
        margin-bottom: 10px;
    }
    .tag-title>strong::before {
        content: "";
        position: absolute;
        bottom: -2px;
        left: 0;
        width: 25px;
        height: 4px;
        background-color: #3780f5;
    }

    .list-tag {
    display: flex;
    flex-wrap: wrap;
    gap: 10px; /* Khoảng cách giữa các thẻ */
    background-color: #ffffff; /* Màu nền */
    padding: 10px; 
    }

.list-tag a {
    display: block;
    padding: 5px 5px; /* Khoảng cách padding bên trong thẻ */
    background-color: #eaeef1; /* Màu nền cho thẻ <a> */
    color: #101010; /* Màu chữ */
    text-decoration: none; /* Loại bỏ gạch chân chữ */
    border-radius: 5px; /* Góc bo tròn */
}

</style>
<script>
export default{
    data() {
        return {
            tags: [
            {
                title: 'ads',
                href: '#'
            },
          
            {
                title: 'adwords',
                href: '#'
            },
          
            {
                title: 'airline',
                href: '#'
            },
          
            {
                title: 'apple',
                href: '#'
            },
          
            {
                title: 'blog',
                href: '#'
            },
          
            {
                title: 'books',
                href: '#'
            },
          
            {
                title: 'design',
                href: '#'
            },
          
            {
                title: 'google',
                href: '#'
            },
          
            {
                title: 'iphone',
                href: '#'
            },
          
            {
                title: 'marketing',
                href: '#'
            },
          
            {
                title: 'page',
                href: '#'
            },
          
            {
                title: 'seo',
                href: '#'
            },
          
            {
                title: 'site',
                href: '#'
            },
          
            {
                title: 'summer',
                href: '#'
            },
          
            {
                title: 'tag',
                href: '#'
            },
          
            {
                title: 'tag one',
                href: '#'
            },
          
            {
                title: 'tag two',
                href: '#'
            },
          
            {
                title: 'tiktok',
                href: '#'
            },


            ]
       
            

        };
    }
}
</script>