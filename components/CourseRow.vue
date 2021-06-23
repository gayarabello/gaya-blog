<template>
  <v-row no-gutters align="center" class="my-1">
    <v-col cols="12" md="3">
      <img
        style="object-fit: contain"
        width="160px"
        height="160px"
        class="pa-3"
        :src="course.image"
        alt="Course Logos"
      />
    </v-col>
    <v-col cols="12" md="9">
      <h3>{{ course.title }}</h3>
      <h5 class="my-2 grey--text">{{ course.subtitle }}</h5>
      <a
        v-for="(link, i) in course.links"
        :key="i"
        class="link my-8 mr-3"
        target="_blank"
        :href="link.url"
        >{{ link.title }}</a
      >
    </v-col>
  </v-row>
</template>
<script>
export default {
  props: { course: { type: Object } }
}
</script>
