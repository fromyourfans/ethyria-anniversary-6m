<template>
  <v-container class="section-grid">
    <v-row no-gutters class="mb-4">
      <v-col cols="12">
        <h1 class="yellow--text text--darken-3 text-center pa-0 ma-0">
          <img
            src="../assets/img/section-mural.png" height="60"
            alt="Drawing Board" />
        </h1>
        <h2 class="grey--text text-center pa-0 ma-0">
          Famillie gathered around a mural to doodle their feelings for Millie
        </h2>
      </v-col>
    </v-row>
    <v-row no-gutters class="px-16">
      <v-col>
        <v-img
          contain
          max-height="94vh"
          @click="onImgClick"
          :src="this.image"  />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import image from '../assets/mural-6months.jpg';

export default {
  props: [],
  data: () => ({
    image,
  }),
  methods: {
    onImgClick() {
      window.open(image);
    },
  },
};
</script>

<style lang="scss" scoped>

</style>
