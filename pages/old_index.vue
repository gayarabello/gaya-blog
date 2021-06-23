<template>
  <div>
    <v-container fluid>
      <v-row class="content-container my-12">
        <v-col cols="12" sm="6">
          <h1>
            <span style="text-decoration: underline #8713F3;"> Bring</span>
            me your challenge so we can grow together
          </h1>
          <div class="py-6" style="color: $blue;">
            <nuxt-link class="link py-6" :to="{ path: '/', hash: 'contact' }">
              Hire me ></nuxt-link
            >
          </div>
        </v-col>
        <v-col cols="12" sm="6" class="text-center">
          <img src="~/assets/images/profile_pic.png" width="240px" />
          <p
            style="font-weight: normal; color: #575757; font-size: 14px; line-height: 150%; letter-spacing: 0.3em; text-transform: uppercase;"
            class="mt-6"
          >
            product designer <br />
            / ux consultant
          </p>
        </v-col>
      </v-row>
      <v-row class="no-gutters my-12 off-section">
        <v-row class="content-container align-start align-md-end py-12">
          <v-col cols="12" md="6">
            <h5 class="py-6">career path and values</h5>
            <h2>The values that brought me here</h2>
            <p class="py-6">
              I rely on a continuous improvement mindset that makes me learn
              everyday and constantly enhance my skillset.
            </p>
          </v-col>
          <v-col cols="12" md="6" class="pb-12">
            <ul>
              <li class="py-4">
                <router-link class="link" to="/me">
                  Get to know my journey >
                </router-link>
              </li>
              <li>
                <router-link class="link" to="/me">
                  Get to know my personal projects >
                </router-link>
              </li>
            </ul>
          </v-col>
        </v-row>
      </v-row>
      <v-row class="content-container">
        <v-col class="text-center" cols="12">
          <h5 class="py-6">case studies</h5>
          <h2>From user research to user interface</h2>
          <p class="py-6">
            User research, journeys, taskflows, wireframing and prototyping. See
            how I manage to validate ideas trought my design process.
          </p>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card class="mx-auto" max-width="400" height="430px">
            <v-img
              class="white--text align-end"
              height="220px"
              src="https://images.unsplash.com/flagged/photo-1573763955714-e7114250fdaa?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2100&q=80"
            >
            </v-img>

            <v-card-subtitle class="pb-0"> #EDUCATIONAL </v-card-subtitle>
            <v-card-text class="py-0 my-0">
              <h4 class="py-4">Ainda estou a aprender</h4>
              <p>
                Educational Platform to help alphabetize young students.
              </p>
            </v-card-text>

            <v-card-actions class="my-0">
              <v-btn
                color="blue"
                text
                to="/blog/2020-04-07-educational-platform"
              >
                See more
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card class="mx-auto" max-width="400" height="430px">
            <v-img
              class="white--text align-end"
              height="220px"
              src="https://early.betmarkets.io/wp-content/uploads/2019/04/concept_v4.jpg"
            >
            </v-img>

            <v-card-subtitle class="pb-0"> #FINTECH </v-card-subtitle>
            <v-card-text class="py-0 my-0">
              <h4 class="py-4">Betmarkets.io</h4>
              <p>
                Sports Betting Investments platform.
              </p>
            </v-card-text>

            <v-card-actions class="my-0">
              <v-btn color="blue" text>
                See case study
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      <v-row class="off-section py-12 mt-12">
        <v-row class="content-container">
          <v-col class="text-center" cols="12">
            <h5 class="py-6">blogposts</h5>
          </v-col>
          <v-col
            cols="12"
            sm="6"
            md="4"
            v-for="(blogPost, index) in blogPosts.slice(0, 3)"
            :key="index"
          >
            <div class="card my-2 pa-0">
              <nuxt-link
                :to="`blog/${blogPost.slug}`"
                style="text-decoration: none!important;"
              >
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
                  <p>
                    {{ blogPost.description }}
                  </p>
                </div>
              </nuxt-link>
            </div>
          </v-col>
          <v-col cols="12" class="text-center">
            <v-btn color="blue" text to="/blog">
              See all Blogposts
            </v-btn>
          </v-col>
        </v-row>
      </v-row>
    </v-container>
  </div>
</template>

<script>
//import Logo from '~/components/Logo.vue'

export default {
  components: {
    //Logo
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }
      ]
    }
  },
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts
    }
  }
}
</script>

<style lang="scss">
@import '~/assets/css/main.scss';

a {
  font-weight: bold;
  color: $blue;
  font-size: 18px;
}

.link {
  color: $blue !important;
}
</style>
