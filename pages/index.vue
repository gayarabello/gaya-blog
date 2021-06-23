<template>
  <div>
    <v-container>
      <v-row no-gutters class="my-12 py-12 text-center" justify="center">
        <v-col cols="12" md="9">
          <h1 class="pt-6">Take a breath, you might be looking at a 🦄</h1>
          <h4 class="py-6">
            A frontend developer with 2 years experience in Javascript, Vuejs,
            Vuex, Nuxt, HTML, CSS and a background in UX/UI design
          </h4>
          <a
            target="_blank"
            class="link pb-6"
            href="https://calendly.com/gaya-correia/15min"
            >Schedule a 15min chat</a
          >
        </v-col>
      </v-row>
    </v-container>
    <div style="background-color: #F5F7FA">
      <v-container class="py-12">
        <h5 class="text-center my-6">about</h5>
        <About :data="about" v-for="about in abouts" :key="about.title" />
      </v-container>
    </div>
    <v-container class="py-12">
      <h5 class="text-center my-6">skills</h5>
      <v-row no-gutters justify="center">
        <v-col cols="12" md="8">
          <h2 class="text-center my-6">
            <span class="font-weight-400">In times of machine learning </span>
            meet a learning machine 😉
          </h2>
        </v-col>
      </v-row>
      <v-row no-gutters justify="center" align="center">
        <v-col cols="12" md="5">
          <table
            class="text-left white pt-3"
            style="width: 100%; max-width: 300px; box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.14);"
          >
            <tr>
              <th class="font-weight-400 grey--text px-4">Skill</th>
              <th class="font-weight-400 grey--text pl-4 text-left">Years</th>
            </tr>
            <tr
              v-for="(skill, i) in skills"
              :key="skill.title"
              :style="i % 2 != 0 ? 'background-color: #F5F7FA' : ''"
            >
              <td class="py-3 pl-4">
                <div class="d-flex align-center">
                  <img
                    style="object-fit: contain"
                    width="24px"
                    height="24px"
                    :src="skill.icon"
                    alt=""
                  />
                  <span class="ml-3">
                    {{ skill.title }}
                  </span>
                </div>
              </td>
              <td class="py-2 pl-4 text-left">{{ skill.years }}</td>
            </tr>
          </table>
        </v-col>
        <v-col cols="12" md="5">
          <p>
            <strong>
              I dedicated the last 10 years educating myself in order to build a
              diverse skillset</strong
            >
          </p>
          <p>
            I am always updating my skillset by watching online courses and
            attending to conferences and meetups on and offline.
          </p>
        </v-col>
      </v-row>
    </v-container>
    <v-container class="py-12 mt-12">
      <h5 class="text-center my-6">work experience</h5>
      <v-row no-gutters justify="center">
        <v-col cols="12" md="8">
          <h2 class="text-center my-6">
            Hands on work for companies and for clients
          </h2>
        </v-col>
      </v-row>
      <h5 class="text-center my-6">in-company employment</h5>
      <v-row
        v-for="work in workExperience"
        :key="work.title"
        class="my-6"
        align="center"
        justify="center"
      >
        <v-col cols="12" md="5">
          <div
            class="d-flex align-center justify-center ml-auto"
            :style="`backgroundColor: ${work.color}`"
            style="max-width: 200px; height: 120px; border-radius: 0.75rem"
          >
            <img height="auto" width="160px" :src="work.image" alt="" />
          </div>
        </v-col>
        <v-col cols="12" md="7">
          <h3>{{ work.title }}</h3>
          <h5 class="my-2 grey--text">{{ work.subtitle }}</h5>
          <a
            v-for="(link, i) in work.links"
            :key="i"
            target="_blank"
            class="link my-8 mr-3"
            :href="link"
            >{{ link }}</a
          >
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <h5 class="text-center my-6">recent client work</h5>
      <h4 class="text-center my-6">
        Landing pages using NuxtJs, Firebase and Analytics
      </h4>
      <v-row class="my-6 " justify="center" align="center">
        <div class="px-4" v-for="work in freelance" :key="work.link">
          <div
            class="d-flex align-center justify-center ml-auto"
            :style="`backgroundColor: ${work.color}`"
            style="min-width: 200px; max-width: 200px; height: 120px; border-radius: 0.75rem"
          >
            <img
              height="auto"
              width="160px"
              class="px-6"
              :src="work.image"
              alt=""
            />
          </div>
        </div>
      </v-row>
    </v-container>
    <v-container class="my-8 my-sm-12 py-8 py-sm-12">
      <h5 class="text-center my-6">testimonials</h5>
      <h2 class="text-center my-6 mx-auto" style="max-width: 750px">
        What my former employers and colleagues have to say about me
      </h2>
      <v-row class="my-6" justify="center" align="center">
        <div class="my-7">
          <svg
            width="32"
            height="24"
            viewBox="0 0 37 32"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0 32H15.0089V16.9911H9.91151L15.8584 0H8.63717L0 18.5487V32ZM20.9558 32H35.9646V16.9911H30.8673L36.8142 0H29.5929L20.9558 18.5487V32Z"
              fill="#333333"
            />
          </svg>

          <p style="max-width: 500px">
            Gaya proved to be a creative, dedicated and collaborative
            professional even working remotely, many years before a pandemic
            forced us to prioritize remote work.
          </p>
          <a target="_blank" class="link" href="">Lino Bocchini</a>
          <span>- Former Director at Entrelinhas</span>
        </div>
      </v-row>
    </v-container>
    <v-container class="my-12">
      <h2 class="text-center my-6 mx-auto" style="max-width: 750px">
        I’m self-taught in many topics, but I had good times in school too 🤓
      </h2>
      <section class="my-12">
        <h5 class="text-center my-6">formal education</h5>
        <div
          v-for="course in courses.filter(e => e.formal)"
          :key="course.title"
        >
          <CourseRow :course="course" />
        </div>
      </section>
      <section class="my-12">
        <h5 class="text-center my-6">Online education</h5>
        <div
          v-for="course in courses.filter(e => !e.formal)"
          :key="course.title"
        >
          <CourseRow :course="course" />
        </div>
      </section>
    </v-container>
  </div>
</template>

<script>
import About from '~/components/About.vue'
import CourseRow from '~/components/CourseRow.vue'

export default {
  components: {
    About,
    CourseRow
  },
  data() {
    return {
      courses: [
        {
          title: 'Specialisation in Interaction Design, Web and Games',
          subtitle: 'SEPTEMBER 2018 - MAY 2019,  PORTO, PORTUGAL',

          links: [
            {
              title: 'Porto University',
              url:
                'https://sigarra.up.pt/fbaup/en/cur_geral.cur_info_cand_view?pv_ano_lectivo=2019&pv_curso_id=17441&pv_origem=CUR&pv_tipo_cur_sigla='
            }
          ],
          image: 'https://sigarra.up.pt/fbaup/pt/imagens/LogotipoSI',
          formal: true
        },
        {
          title: 'Bachelor in Advertising / Social Communication',
          subtitle: 'FEBRUARY 2008 - DECEMBER 2011,  RIO DE JANEIRO, BRAZIL',

          links: [
            {
              title: 'Pontifical Catholic University of Rio de Janeiro',
              url: 'https://www.puc-rio.br/index.html'
            }
          ],
          image: 'https://www.puc-rio.br/imagens/bras_83x140_reduzido.png',
          formal: true
        },
        {
          title: 'JavaScript Algorithms and Data Structures',
          subtitle: 'JUNE  2020 - PRESENT,  ONLINE',
          links: [
            {
              title: 'FreeCodeCamp',
              url: 'https://www.freecodecamp.org/gayacorreia'
            }
          ],
          image: 'https://popsql.com/static/external-logos/freecodecamp.png',
          formal: false
        },
        {
          title: 'Vue and Nuxt.js',
          subtitle: 'JANUARY 2020, PRESENT, ONLINE',
          links: [
            {
              title: 'Vue School',
              url: 'https://vueschool.io/'
            },
            {
              title: 'Vue Mastery',
              url: 'https://www.vuemastery.com/'
            }
          ],
          image:
            'https://i.pinimg.com/originals/94/1c/36/941c36f973c0eac1c6bd41e3388aa2c0.png',
          formal: false
        },
        {
          title: 'Javascript, HTML and CSS',
          subtitle: 'NOVEMBER 2018,  PORTO, PORTUGAL',
          links: [
            {
              title: 'Certificate',
              url:
                'https://www.shecodes.io/certificates/a5f3031427753a0a90090035ae08e9b7'
            },
            {
              title: 'She Codes',
              url: 'https://www.shecodes.io/students/gaya-rabello'
            }
          ],
          image:
            'https://www.shecodes.io/assets/branding/logo-shecodes-f9fa0540d113c086f61eb6e89466c0cbd24a42163b6a96d4b01da078803f53ee.png',
          formal: false
        }
      ],

      freelance: [
        {
          link: 'kaeser.digital',
          image: 'https://pt.kaeser.com/Media/logo_35-52130-130x40%402x.png',
          color: '#FFCF01'
        },
        {
          link: 'oportocollection.com',
          image: 'https://pt.kaeser.com/Media/logo_35-52130-130x40%402x.png',
          color: '#264F8D'
        }
      ],
      workExperience: [
        {
          title: 'Frontend Developer',
          subtitle: 'OCTOBER 2018 - PRESENT,  UPTEC - PORTO',
          image:
            'https://res.cloudinary.com/betmarkets/image/upload/v1567614196/branding/betmarkets_light_logo_notagline_i63shv.png',
          links: ['betmarkets.io', 'app.betmarkets.io'],
          color: '#29313A'
        },
        {
          title: 'Creative Director',
          subtitle: 'AUGUST 2016 - AUGUST 2019,  BRASILIA',
          image:
            'https://static.wixstatic.com/media/92438a_75bd72c379aa4411b9cec34373b91495~mv2.png/v1/fill/w_280,h_89,al_c,lg_1,q_85/92438a_75bd72c379aa4411b9cec34373b91495~mv2.webp',
          links: ['nobot.com.br'],
          color: '#333333'
        },
        {
          title: 'Art Director',
          subtitle: 'AUGUST 2016 - AUGUST 2019,  BRASILIA',
          image:
            'http://www.entrelinhas.net/novo/wp-content/themes/Entrelinhas/library/images/logo.png',
          links: ['entrelinhas.net'],
          color: '#A10B0F'
        }
      ],

      skills: [
        {
          icon:
            'https://cdn.icon-icons.com/icons2/2108/PNG/512/javascript_icon_130900.png',
          title: 'Javascript ES6',
          years: 2
        },
        {
          icon:
            'data:image/png;base64,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',
          title: 'Vue and Nuxt.js',
          years: 2
        },
        {
          icon:
            'data:image/png;base64,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',
          title: 'HTML5',
          years: 2 + '+'
        },
        {
          icon:
            'https://sass-lang.com/assets/img/styleguide/color-1c4aab2b.png',
          title: 'CSS and SASS',
          years: 2 + '+'
        },
        {
          icon:
            'data:image/png;base64,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',
          title: 'Adobe Suite',
          years: 8 + '+'
        },
        {
          icon: 'https://cdn.worldvectorlogo.com/logos/figma-1.svg',
          title: 'Figma',
          years: 2 + '+'
        }
      ],
      abouts: [
        {
          title: 'Why Frontend?',
          image:
            'https://images.unsplash.com/photo-1596003906949-67221c37965c?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8cHJvZ3JhbW1lcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60',
          subtitle:
            'As a former UX/UI designer, I wanted to be able to display my dribbble shots coded in the browser.'
        },
        {
          title: 'What Drives Me',
          image:
            'https://images.unsplash.com/photo-1423784346385-c1d4dac9893a?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          subtitle:
            'I’m driven by an optimization passion. I don’t go for workarounds, and I don’t stop until I find the root cause. Read what my former employers and colleagues have to say about me.'
        },
        {
          title: 'Current Projects',
          image:
            'https://images.unsplash.com/photo-1502945015378-0e284ca1a5be?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80',
          subtitle:
            'I am currently freelancing for a hospitality portuguese group. I’m also coding a PWA to help people keep on track with their sugar intake.'
        }
      ]
    }
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

tr {
  padding: 1rem;
}

a {
  font-weight: bold;
  color: $blue;
  font-size: 18px;
}

.container {
  max-width: 56rem;
}

.link {
  color: $blue !important;
}
</style>
