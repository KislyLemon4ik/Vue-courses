<template>
    <div class="app">
        <PostForm @add="addArray"/>
        <PostList :posts="posts"/>
    </div>
    
</template>

<script>
import PostForm from "@/components/PostForm.vue"
import PostList from "@/components/PostList.vue"

export default {
    components: {
        PostForm, PostList
    },
    data() {
        return {
           posts: [
            {id:1, title: 'JavaScript', body: 'Описание поста'},
            {id:2, title: 'Vue', body: 'Описание Vue'}
           ]
        }
    },
    
    methods: {
        addArray(post) {
            this.posts.push(post);
            console.log(this.post);
        }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}


</style>