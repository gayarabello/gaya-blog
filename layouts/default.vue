<template>
  <v-app light>
    <!--     <v-banner class="banner" dark>
      I'm donating 8 hours per week of my work to non-profit health-related
      projects.
      <template v-slot:actions>
        <v-btn color="white" text>reach me out</v-btn>
      </template>
    </v-banner> -->
    <v-row no-gutters class="banner py-3">
      <v-row
        no-gutters
        class="content-container justify-space-between align-center px-8 px-md-0"
      >
        <p class="mb-0 banner">
          Hello, friend
        </p>
        <p class="mb-0 banner">
          <nuxt-link
            class="banner"
            style="color: white;"
            dark
            :to="{ path: '/', hash: 'contact' }"
          >
            Let's talk</nuxt-link
          >
        </p>
        <!-- <v-btn color="white" text dark> reach me </v-btn> -->
      </v-row>
    </v-row>

    <v-app-bar flat height="80px" style="max-height: 80px;">
      <v-row class="align-center content-container justify-space-between">
        <v-col>
          <nuxt-link class="logo" to="/">Gaya </nuxt-link>
        </v-col>
        <div>
          <nuxt-link class="nav-item" to="/me">
            <span>
              Me
            </span>
          </nuxt-link>
          <nuxt-link class="nav-item" to="/blog"><span> Blog </span></nuxt-link>
          <nuxt-link class="nav-item" :to="{ path: '/', hash: 'contact' }">
            <span> Talk </span>
          </nuxt-link>
        </div>
      </v-row>
    </v-app-bar>
    <nuxt />
    <v-row
      no-gutters
      id="contact"
      class="py-8 mb-0"
      style="background-color: #191919"
    >
      <v-row class="content-container justify-center justify-space-between">
        <v-col class="mx-auto" cols="10" md="6">
          <h5 style="color: grey;" class="py-6">Let's talk</h5>
          <h2 style="color: white;" class="mb-4">
            Bring me your challenge so we can grow together
          </h2>
          <h4 class="link">
            talktogaya@gmail.com
          </h4>
          <p style="color: grey;" class="py-6 d-none d-sm-block">
            2020 | This website is open source
          </p>
        </v-col>

        <v-col class="mx-auto" cols="10" md="4">
          <h5 style="color: grey;" class="pt-6 pb-2">see also</h5>
          <ul class="pl-0" style="list-style: none;">
            <li class="py-4">
              <router-link class="link" :to="{ path: '/me', hash: 'skillset' }">
                Skillset
              </router-link>
            </li>
            <li>
              <router-link class="link" to="/me">
                Career Path
              </router-link>
            </li>
            <li class="py-4">
              <router-link class="link" to="/contact">
                Case Studies
              </router-link>
            </li>
            <li class="pb-4">
              <router-link class="link" to="/contact">
                Personal Projects
              </router-link>
            </li>
            <li>
              <router-link class="link" to="/blog">
                Blog
              </router-link>
            </li>
          </ul>
        </v-col>
      </v-row>
    </v-row>
  </v-app>
</template>

<style lang="scss">
@import '~/assets/css/main.scss';

/* *,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
} */

.nav-item {
  margin-right: 1rem;
  color: #333333;
  text-decoration: none !important;
}

.logo {
  color: #333333;
  font-size: 2rem;
  text-decoration: none;
}
</style>
