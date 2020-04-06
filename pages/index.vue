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
            <nuxt-link class="link py-6" to="/contact"> Hire me ></nuxt-link>
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
      <v-row class="no-gutters my-12" style="background-color: #fafafa;">
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
                <router-link class="link" to="/contact">
                  Get to know my journey >
                </router-link>
              </li>
              <li>
                <router-link class="link" to="/contact">
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
              <!-- <v-card-title> <h4>Ainda estou a aprender</h4></v-card-title> -->
            </v-img>

            <v-card-subtitle class="pb-0"> #EDUCATIONAL </v-card-subtitle>
            <v-card-text class="py-0 my-0">
              <h4 class="py-4">Ainda estou a aprender</h4>
              <p>
                Educational Platform to help alphabetize young students.
              </p>
            </v-card-text>

            <v-card-actions class="my-0">
              <v-btn color="blue" text>
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
              <!-- <v-card-title> <h4>Ainda estou a aprender</h4></v-card-title> -->
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
  }
}
</script>

<style lang="scss">
@import '~/assets/css/main.scss';

/* .title {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
    'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: bold;
  font-size: 3.2rem;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 2rem;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
} */
a {
  font-weight: bold;
  color: $blue;
  font-size: 18px;
}

.link {
  color: $blue !important;
}
</style>
