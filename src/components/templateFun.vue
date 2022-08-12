<template>
  <div>
    <button @click="set_show">show</button>
    <div v-if="show_post === true">
    <div v-for="(post,index) in posts" :key="index">
        <h1>{{post[`blog_title`]}}</h1>
        <p>{{post[`blog_content`]}}</p>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    set_show() {
      this.show_post = !this.show_post;
    },
  },
  data() {
    return {
      posts: [
        {
          blog_content: `This is the content_one for the blog`,
          blog_title: `Title_one`,
        },
        {
          blog_content: `This is the content_two for the blog`,
          blog_title: `Title_two`,
        },
        {
          blog_content: `This is the content_three for the blog`,
          blog_title: `Title_three`,
        },
      ],

      show_post: false,
    };
  },
};
</script>

<style scoped>
div {
  text-align: center;
}
</style>