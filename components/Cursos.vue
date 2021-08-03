<template>
  <section>
  <h1>Cursos</h1>
  <div style="display: none;">{{getPosts()}}</div>
    <div style="width: 45vw; margin-botton: 2vw;" v-for="(post, index) in posts" :key="index">
      <h2>{{post.title.rendered}}</h2><br />
      <a target="_blank" :href="post.link"><div class="posts-corpo" v-html="post.excerpt.rendered"></div></a>
    </div>
  </section>
</template>
<script>
export default {
  data(){
    return {
      api: "https://cursoscaduceu.com.br/wordpress/wp-json/wp/v2/posts?_fields=author,id,excerpt,title,link",
      posts: [],
    }
},
  methods: {
    async getPosts() {
    const posts = await this.$axios.$get(this.api)
    this.posts = JSON.parse(JSON.stringify(posts))
  }
    },
}
</script>
<style scoped>
.more-link, .posts-corpo > a{
  color: rgb(0, 81, 255);
}
</style>
