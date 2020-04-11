<template>
  <div>
    <v-row class="content-container">
      <v-col cols="12" class="my-8 text-center">
        <h1>
          Blog
        </h1>
        <h4 class="py-5">
          Get to know a bit about my learning and work experience
        </h4>
      </v-col>
      <v-row class="justify-space-between px-8">
        <v-col
          cols="12"
          sm="6"
          md="4"
          v-for="(blogPost, index) in blogPosts"
          :key="index"
        >
          <div class="card my-2 pa-0">
            <nuxt-link :to="`blog/${blogPost.slug}`">
              <div
                style="text-decoration: none !important;"
                class="thumbnail d-flex align-end"
                :style="{
                  backgroundImage: `linear-gradient(rgba(17, 17, 17, 0), #262D34 100%), url(${blogPost.thumbnail})`
                }"
              >
                <h3 class="pa-4 text-white">
                  {{ blogPost.title }}
                </h3>
              </div>
              <div class="pa-4">
                <p>{{ blogPost.description }}</p>
              </div>
            </nuxt-link>
          </div>
        </v-col>
      </v-row>
    </v-row>
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

<style lang="scss" scoped>
a {
  text-decoration: none !important;
}

p {
  text-decoration: none !important;
}
</style>
