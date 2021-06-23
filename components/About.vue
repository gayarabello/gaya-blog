<template>
  <v-row class="my-3" justify="center" align="center">
    <v-col cols="3">
      <img
        class="image--cover"
        height="160px"
        width="100%"
        :src="data.image"
        alt=""
      />
    </v-col>
    <v-col cols="6">
      <h3 class="pt-6">{{ data.title }}</h3>
      <p class="py-6">
        {{ data.subtitle }}
      </p>
    </v-col>
  </v-row>
</template>
<script>
export default {
  props: {
    data: {
      type: Object
    }
  }
}
</script>
