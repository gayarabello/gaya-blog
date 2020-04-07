<template>
  <article class="px-8">
    <v-row class="content-container my-6">
      <nuxt-link :to="'/blog'"> back to blog</nuxt-link>
    </v-row>
    <v-row class="content-container mt-12">
      <h1>{{ blogPost.title }}</h1>
      <div class="pt-12" v-html="$md.render(blogPost.body)" />
    </v-row>
  </article>
</template>
<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { blogPost: payload }
    else
      return {
        blogPost: await require(`~/assets/content/blog/${params.blog}.json`)
      }
  }
}
</script>
