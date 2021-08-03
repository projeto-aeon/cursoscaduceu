<template>
  <section>
  <h1>Cursos</h1>
  <div>{{getPosts()}}</div>
    <div v-for="(post, index) in posts" :key="index">
      {{post}}
    </div>
  </section>
</template>
<script>
export default {
  data(){
    return {
      api: "https://cursoscaduceu.com.br/wordpress/wp-json/wp/v2/posts",
      posts: [],
    }
},
  methods: {
    async getPosts() {
    const posts = await this.$axios.$get("https://cursoscaduceu.com.br/wordpress/wp-json/wp/v2/posts", { headers: {'Access-Control-Allow-Origin': "*"} })
    this.posts = posts
  }
    },
}
</script>
