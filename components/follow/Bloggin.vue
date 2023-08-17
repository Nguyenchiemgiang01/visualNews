<template>
    <div class="bloggin">

        <div class="follow" style="margin-top: 10px;">
            <strong>BLOGGING</strong>
        </div>

        <div class="">
            <div class="postcart">
                <Typetag
                    image="https://demo.wpenjoy.com/visualnews-pro/wp-content/uploads/sites/64/2023/06/solar-panels_EFYB8VJXNT.jpg"
                    title="Why Apple Vision Pro’s $3,499 Price Makes More Sense Than You Think" />
            </div>
        </div>


    </div>
</template>
<script>
import Typetag from ".././typetag/index.vue"
export default {
    components: { Typetag }
}
</script>

<style scoped>
@media (max-width:760px) {
    .bloggin{
        margin-top: 40px;
    }
 


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

}

@media (min-width:1200px) {


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


    .bloggin{
        margin-top: 40px;
    }






}
</style>