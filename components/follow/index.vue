<template>
    <div class="follow-right-page">
        <Follow />
        <Blogging />
        <Advertisting/>
        <Fashion/>
    </div>
     
     
</template>

<script>
    import Follow from "./Follow.vue"
    import Advertisting from "./Advertisting.vue"
    import Fashion from "./Fashion.vue"
    import Blogging from "./Bloggin.vue"

    export default{
        components:{Follow,Advertisting,Fashion,Blogging}
    }
</script>
<style>
</style>