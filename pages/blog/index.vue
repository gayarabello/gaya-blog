<template>
  <div>
    <ul v-for="(blogPost, index) in blogPosts" :key="index">
      <img width="200px" :src="blogPost.thumbnail" />
      <nuxt-link :to="`blog/${blogPost.slug}`">{{ blogPost.title }}</nuxt-link>
      <p>{{ blogPost.description }}</p>
    </ul>
  </div>
</template>
<script>
export default {
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts
    }
  }
}
</script>
