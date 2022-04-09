<template>
  <v-container class="section-grid section-box pb-8">
    <v-row no-gutters class="pt-8">
      <v-col cols="6"
        class="text-right white--text text-h5 text--darken-1 pt-4 pr-8 pl-4 hero-text">
        <p>
          Happy 6 month anniversary Millie!
          The FaMillie have gotten together to create this incredible website filled with
          clips, art, and messages just for you!
          From the bottom of our hearts, thank you for bringing joy to
          our days and we hope you enjoy everything!
        </p>
      </v-col>
      <v-col cols="6" class="pr-8 text-center grey--text text--lighten-1">
        <iframe title="feature-video"
          width="100%" height="330"
          src="https://www.youtube.com/embed/ygS22EC6u2c?mute=1"
          frameborder="0"
          allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
          allowfullscreen>
        </iframe>
        <h5>
          Stream Caution: Part of video contains Titanic flute music.<br />
          Video will start muted. Unmute at will.
        </h5>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: [],
  data: () => ({
    //
  }),
};
</script>

<style lang="scss" scoped>
.section-grid {
  margin-top:340px;
  max-width:1280px;
  .hero-text {
    white-space: pre-line;
  }
}
</style>
