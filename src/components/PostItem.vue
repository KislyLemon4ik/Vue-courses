<template>
    <div class="post">
        <div>Название: {{ post.title }} Описание: {{ post.body }}</div>
    </div>
</template>

<script>
export default{
    props: {
        post:{
            title: '',
            body: '',
            required: true,
        }
    }
}
</script>

<style scoped>
.post{
    padding: 15px;
    margin-top: 15px;
    border: 4px solid teal;
}
</style>