<template>
    <div> 
        <h3>Список пользователей</h3>
        <PostItem class="post" v-for="post in posts" :post="post" />
    </div>
    
    
</template>

<script>
import PostItem from './PostItem.vue';

export default{
    components: {
        PostItem
    },
    props: {
        posts: {
            type: Array,
            required: true,
        }
    },
    components: { PostItem }
} 

</script>
    
<style scoped>
.post{
    padding: 15px;
    margin-top: 15px;
    border: 4px solid teal;
}
</style>