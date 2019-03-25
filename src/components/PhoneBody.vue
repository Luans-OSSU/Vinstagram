<template>
    <div class="phone-body">
       <div class="feed">
           <vinstagram-post
                v-for="post in posts"
                :post="post"
                :key="posts.indexOf(post)"
           >
           </vinstagram-post>
       </div>
    </div>
</template>

<script>

import VisntagramPost from "./VinstagramPost";

export default {
    name: "PhoneBody",
    props: {
        posts: Array,
        filters: Array
    },
    components: {
        "vinstagram-post": VisntagramPost
    }
}

</script>


<style lang="scss" src="../styles/phone-body.scss"></style>