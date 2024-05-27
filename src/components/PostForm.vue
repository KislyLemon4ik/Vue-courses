<template>
    <form>
        <h4>Добавление</h4>
        <input v-model="post.title" type="text" placeholder="Название">
        <input v-model="post.body" type="text" placeholder="Описание">
    </form>
    <button class="myButton" @click="addLine">Добавить</button>

</template>

<script>
export default {
    data(){
        return{
            post: {
                title: '',
                body: ''
            }
        }
    },
    methods:{
        addLine() {
            this.post.id = Date.now();
            this.$emit('add', this.post); // Сначала отправляем данные
            this.post = {
                title: '',
                body: ''
            }
        }
        
    }
}
</script>

<style scoped>
.myButton{
    
}
</style>