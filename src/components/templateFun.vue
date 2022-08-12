<template>
  <div>
    <button @click="set_show">show</button>
<h1>{{blog_title}}</h1>
<p v-if="show_post === true">{{blog_content}}</p>
<img :src="blog_image_url" alt="random_image"/>
  </div>
</template>

<script>
export default {
    mounted(){

    },
    methods:{
        set_show(){
            if(this.show_post === true){
                this.show_post = false;
            } else if(this.show_post === false){
                this.show_post = true;
            }
        }
    },
    data() {
        return {
            blog_content: `This is the content for the blog`,
            blog_title : `A Title`,
            blog_image_url: `https://images.unsplash.com/photo-1659806095284-8c9d1ccfc7ef?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHx0b3BpYy1mZWVkfDd8NnNNVmpUTFNrZVF8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60`,
            show_post: true

        }
    },

};
</script>

<style scoped>
div{
    text-align: center;
}
</style>