
<template>
    <div class="layout">
        <Header />
        <div class="primary-content">

            <div class="content-wrapper">



                <div class="content" style="padding-right: 20px;">
                    <div class="main-title">
                        <NuxtLink :to="getCategoryLink">
                            <p style="padding: 2px 2px;font-size: small;background-color: black;color:aliceblue;width: fit-content;font-weight: lighter;margin-top:30px;margin-bottom: 10px;">
                            {{ $route.query.category }}</p>
                        </NuxtLink>

                        

                        <h2>{{ $route.query.title }}</h2>
                        <p style="font-weight: lighter;margin-top: 20px; margin-bottom: 10px;">Posted by {{
                            $route.query.author }} - {{ $route.query.day }} </p>
                        <img :src="$route.query.image" alt="">

                    </div>

                    <div class="entry-content wp-block-post-content is-layout-constrained">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sagittis non libero ac
                            cursus.
                            Duis&nbsp;<a
                                href="https://demo.wpenjoy.com/visualnews/full-width-page/#">sollicitudin</a>&nbsp;nibh eget
                            nisi rhoncus congue. Etiam pellentesque dolor lorem. Praesent cursus nunc ut mauris rhoncus,
                            vitae sagittis
                            est luctus. Nam elementum iaculis commodo. Morbi imperdiet ultrices libero hendrerit venenatis.
                            Curabitur
                            sit amet auctor eros. Phasellus at venenatis eros. Pellentesque vestibulum justo ut augue
                            fringilla commodo.
                            Integer malesuada augue a odio mattis, et efficitur augue vestibulum. Morbi eget volutpat urna.
                            Nam eget
                            eros turpis. Maecenas consequat nulla metus, vel interdum lectus finibus at.</p>
                        <p>Sed consequat nibh nec dui placerat, non viverra ante interdum. Nulla rhoncus enim at orci
                            venenatis, at
                            imperdiet mi interdum. Pellentesque blandit euismod libero, facilisis elementum ante vestibulum
                            et.
                            Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                            Nam fringilla
                            purus vitae quam pretium, sodales commodo neque tincidunt. Nulla nec lorem sed velit suscipit
                            feugiat. Nunc
                            a euismod massa, non tempor nibh. Suspendisse hendrerit iaculis tortor, et accumsan neque
                            dignissim nec.
                            Duis viverra dui mi, quis rutrum neque dapibus ac. Pellentesque porta elit ex, eget volutpat
                            urna malesuada
                            vitae. Nunc et commodo sem. Vivamus non sapien non nulla auctor tempus non nec orci. Nunc
                            laoreet, lacus ut
                            commodo porta, purus urna imperdiet orci, et facilisis nisl lectus non diam. Ut mollis malesuada
                            consectetur. Cras fermentum velit nec ante maximus pellentesque.</p>
                        <p>Suspendisse convallis, sem id vestibulum aliquet, nibh eros sollicitudin ipsum, in semper dolor
                            nisi at ex.
                            Sed non blandit lorem. Aenean et ultricies erat, vitae dictum orci. Orci varius natoque
                            penatibus et magnis
                            dis parturient montes, nascetur ridiculus mus. Phasellus quis nisl volutpat, mattis dui ut,
                            condimentum
                            libero. Morbi et quam eget ipsum consequat pharetra. Integer porttitor vehicula nisi, sit amet
                            euismod purus
                            faucibus eget. Cras faucibus est sem, non consectetur lorem auctor ac. Maecenas tristique metus
                            ante, a
                            tempus lacus luctus nec. Praesent congue nulla quis mi condimentum faucibus. Aliquam vitae orci
                            mattis
                            sapien dignissim euismod. Donec et augue finibus, posuere nibh facilisis, viverra odio. Etiam ut
                            tempus
                            orci, id elementum lorem. Fusce vestibulum, urna quis volutpat tempor, libero nisl tincidunt
                            neque, eget
                            porta est metus id sapien.</p>
                        <p>Aliquam nec convallis nunc. Fusce vehicula varius turpis, et pretium arcu sagittis a. In hac
                            habitasse
                            platea dictumst. Morbi faucibus diam purus, quis aliquet urna mattis in. Donec convallis nec leo
                            ac aliquet.
                            Proin lectus erat, congue a orci at, vestibulum pretium diam. Suspendisse fermentum massa quis
                            pretium
                            commodo.</p>
                        <p>Vivamus vel consectetur ex, vitae commodo sapien. Vestibulum a mollis felis. Phasellus ipsum
                            orci, accumsan
                            nec urna ac, egestas semper enim. Ut malesuada efficitur ante, faucibus rutrum diam. Nullam orci
                            justo,
                            euismod sit amet consectetur ut, porta eget arcu. Duis a ante rutrum, hendrerit eros in,
                            fringilla ante. Sed
                            magna massa, dictum vel enim quis, consequat ultricies dui. Quisque nec magna molestie turpis
                            suscipit
                            lacinia vitae at risus. Fusce tristique orci quam, et vehicula dolor luctus ut. Ut vitae
                            porttitor arcu.
                            Proin aliquet, turpis sit amet auctor dictum, tellus sapien viverra mauris, a dapibus quam leo
                            non tortor.
                            Aenean blandit dapibus urna eget finibus. Morbi sit amet neque ut neque bibendum eleifend ac nec
                            erat. Proin
                            auctor lacus id finibus vehicula. Sed vitae est felis.</p>

                    </div>

                    <div class="tag" style="margin-top: 20px;">
                        <a style="padding: 2px 5px;background-color: #f8f2f2;margin-right: 10px;" href=""> Tag one </a>
                        <a style="padding: 2px 5px;background-color: #f8f2f2;" href="">Tag two</a>

                    </div>

                    <div class="" style="margin-top: 50px;">



                        <div class="author-post"
                            style="padding: 10px 10px;margin-top: 10px; display: block;border: 1px solid #bdb9b9;">
                            <div class="" style="display: flex;align-items: center;">
                                <div class="" style="margin-right: 15px; border-radius: 50%;"><img alt=""
                                        src="https://gravatar.wpenjoy.com/avatar/aed1547d950cb2ba8534a6df5915786f?s=48&amp;d=mm&amp;r=g"
                                        srcset="https://gravatar.wpenjoy.com/avatar/aed1547d950cb2ba8534a6df5915786f?s=96&amp;d=mm&amp;r=g 2x"
                                        class="avatar avatar-48 photo" height="48" width="48" loading="lazy"
                                        decoding="async"></div>
                                <div class="">
                                    <p class="">{{ $route.query.author }}</p>
                                </div>
                            </div>
                            <div class="y">Your introduction goes here. Lorem ipsum dolor
                                sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et
                                dolore magna aliqua.
                            </div>
                        </div>

                    </div>

                    <div class="" style="margin-top: 30px;">
                        <div class="">
                            <h3 class="e" style="font-weight: bolder; margin-bottom: 10px;">Leave a Reply </h3>

                            <form action="" method="" class="comment-form">
                                <p class="comment-notes"><span id="email-notes">Your email address will not be
                                        published.</span> <span class="required-field-message">Required fields are marked
                                        <span class="required">*</span></span></p>

                                <p class="comment-form-comment" style="display: flex;flex-direction: column; order: 1;">
                                    <label for="comment">Comment <span
                                            class="required">*</span></label>
                                    <textarea style="border: 1px solid #bdb9b9;" name="comment" cols="45" rows="8"
                                        maxlength="65525" required=""></textarea>

                                </p>

                                <p class="comment-form-author" style="display: flex;flex-direction: column; order: 1;">
                                    <label for="author">Name
                                        <span class="required">*</span>
                                    </label>
                                    <input  style="border: 1px solid #bdb9b9;" id="author" name="author" type="text" value="" size="30" maxlength="245"
                                        autocomplete="name" required="">
                                </p>
                                <p class="comment-form-email" style="display: flex;flex-direction: column; order: 1;">
                                    <label for="email">Email <span
                                            class="required">*</span></label> <input  style="border: 1px solid #bdb9b9;" id="email" name="email" type="email"
                                        value="" size="30" maxlength="100" aria-describedby="email-notes"
                                        autocomplete="email" required=""></p>
                                <p class="comment-form-url" style="display: flex;flex-direction: column; order: 1;">
                                    <label for="url">Website</label> <input  style="border: 1px solid #bdb9b9;" id="url" name="url"
                                        type="url" value="" size="30" maxlength="200" autocomplete="url"></p>
                                <p class="comment-form-cookies-consent" style="display: flex;flex-direction: row; order: 1;">
                                    <input id="" name="" type="checkbox" value="yes" >
                                        <label
                                        for="">Save my name, email, and website in this browser
                                        for the next time I comment.
                                    </label></p>
                                <p class="" style="color:#ffffff; background-color: #35aed6;width: fit-content; padding: 5px 5px;margin-top: 20px;">
                                    <input name="submit" type="submit" id="submit"
                                        class="" value="Post Comment"> <input
                                        type="hidden" name="comment_post_ID" value="272" id="comment_post_ID">
                                    <input type="hidden" name="comment_parent" id="comment_parent" value="0">
                                </p>
                            </form>
                        </div>
                    </div>

                </div>



                <div class="follow" style="margin-left: 10px;">
                    <form class="search-form" action="" method="">
                        <input style="background-color:#f1f1f1;width: 188px;height: 36px;" type="text" name="query"
                            placeholder="Search for">
                        <button style="background-color: rgb(16, 164, 218); width: 82px;height:  36px;"
                            type="submit">Search</button>
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

import PostDetail from '../../components/typepost/postdetail.vue'
import Header from '../../layout/Header';
import Content from '../../components/content/Content.vue';
import Follow from '../../components/follow/Follow.vue';
import Fashion from '../../components/follow/Fashion.vue';
import Business from '../../components/business/index.vue';
import Categoryname from '../../components/typepost/catagoryname.vue';
import Tag from '../../components/tag/tag.vue'

import Footer from "../../layout/Footer"

export default {
    computed: {
    getCategoryLink() {
      const category = (this.$route.query.category).toLowerCase();
      return `/${category}`;
    },
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
    form p {
    margin-top: 20px; /* Khoảng cách trên */
    margin-bottom: 20px; /* Khoảng cách dưới */
}
    input {
        height: 50px;
    };

    p {
        font-size: 17px;
    }

    .main-title {
        margin-bottom: 30px;
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

}
</style>
  