<template>
  <div>
    <v-container fluid>
      <v-row class="content-container my-12">
        <v-col cols="12" sm="6">
          <h1>
            About Me
          </h1>
          <div class="py-6" style="color: $blue;">
            <nuxt-link class="link py-6" to="/contact"> Hire me ></nuxt-link>
          </div>
        </v-col>
        <v-col cols="12" sm="6" class="text-center">
          <img src="~/assets/images/me.jpg" width="100%" />
          <p
            style="font-weight: normal; color: #575757; font-size: 14px; line-height: 150%; letter-spacing: 0.3em; text-transform: uppercase;"
            class="mt-6"
          >
            product designer <br />
            / ux consultant
          </p>
        </v-col>
      </v-row>
      <v-row class="content-container py-6">
        <v-col cols="12">
          <h2 class="my-6">Carrer Path</h2>
          <p>
            🎓 2011- Graduated in Advetisement
          </p>
          <p>
            🎨 2011 - 2017 - Graphic Designer/Art Director in multiple design
            and adverstisement studios
          </p>
          <p>
            🔥 2014 - Art Director in Brazilian biggest political party scaled
            for the presidencial campaign
          </p>
          <p>
            🖥 2015 - Started designing landing pages for events, campaigns and
            institucional static websites
          </p>
          <p>
            🖥 2016 - Started learning UX online on Lynda.com
          </p>
          <p>
            🤓 2018 - Attended a postDegree in Interaction Design, started as
            learning HTML/CSS/JS and began working as a intern to Betmarkets.
          </p>
          <p>
            🎉 2019 - Promoted to Product Owner
          </p>
          <p>
            💻 2020 - Assumed Frontend role
          </p>
        </v-col>
      </v-row>
      <v-row id="skillset" class="content-container py-8">
        <v-col cols="12">
          <h2 class="my-6">Skillset</h2>
          <v-row class="align-center">
            <img class="ml-2" src="~/assets/images/icons/ux.png" width="32px" />
            <h5 class="my-6 ml-2">user experience</h5>
          </v-row>
          <p>
            User research, journeys, taskflows, wireframing and prototyping.
            Check my <a class="link" href="/blog"> case studies</a> to see how I
            manage to validate ideas trought my design process.
          </p>

          <div class="my-12">
            <v-row class="align-center">
              <img src="~/assets/images/icons/dribbble.png" height="32px" />
              <h5 class="my-6 ml-2">visual design</h5>
            </v-row>
            <p>
              Form follows function. Once the flow decisions are made it's time
              to dress up the product with the brand visual voice.
              <a class="link" href="/blog"> See here</a> how I create and
              mantain style guides.
            </p>
            <span style="color: #828282">My UI toolset</span>
            <v-row
              style="width: 320px"
              class="justify-space-between align-center my-4 ml-1"
            >
              <img
                src="~/assets/images/icons/visual/sketch.png"
                height="48px"
              />
              <img src="~/assets/images/icons/visual/figma.png" height="44px" />
              <img src="~/assets/images/icons/visual/xd.png" height="36px" />
              <img src="~/assets/images/icons/visual/ps.png" height="36px" />
              <img src="~/assets/images/icons/visual/ai.png" height="36px" />
            </v-row>
          </div>
          <div class="my-12">
            <v-row class="align-center">
              <img
                class="ml-2"
                src="~/assets/images/icons/codepen.png"
                width="32px"
              />
              <h5 class="my-6 ml-2">coding</h5>
            </v-row>
            <p>
              I am absolutly passionate about coding. I'm consistently improving
              my conding skills. Check here my
              <a class="link" href="/blog"> code lab</a>.
            </p>
            <span style="color: #828282">My coding toolset</span>
            <v-row
              style="width: 320px"
              class="justify-space-between align-center my-4 ml-1"
            >
              <img src="~/assets/images/icons/coding/html.png" height="40px" />
              <img src="~/assets/images/icons/coding/css.png" height="40px" />
              <img src="~/assets/images/icons/coding/sass.png" height="40px" />
              <img src="~/assets/images/icons/coding/nuxt.png" height="40px" />
              <img src="~/assets/images/icons/coding/vue.png" height="40px" />
            </v-row>
          </div>
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
              <li>
                <router-link class="link" to="/contact">
                  Get to know my personal projects >
                </router-link>
              </li>
            </ul>
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
