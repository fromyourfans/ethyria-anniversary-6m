<template>
  <v-container class="section-grid pb-8">
    <v-row no-gutters class="mb-4">
      <v-col cols="12">
        <h1 class="yellow--text text--darken-3 text-center pa-0 mx-0 my-">
          <img
            src="../assets/img/section-happy.png" width="700"
            alt="Happy 6-Months and 200K Enna Alouette!" />
        </h1>
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col cols="6"
        class="text-right text-h5 pt-4 pr-8 pl-8 hero-text">
        <p>
          From her funny antics to inspiring stories,
          from questionable comebacks to wholesome moments,
          from scuffed streams to showcasing her amazing voice,
          Enna is a harmony of beautiful personalities.
        </p>
        <p>
          For 6 months we have listened to this wonderful melody thats is Enna.
          We all only hope to experience it for as long as it is to hear,
          a music not only to our ears, but to our hearts.
        </p>
      </v-col>
      <v-col cols="6" class="pr-8">
        <iframe title="feature-video"
          width="100%" height="330"
          src="https://www.youtube.com/embed/Kgqa5NLSM5g?mute=1"
          frameborder="0"
          allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
          allowfullscreen>
        </iframe>
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
  margin-top:400px;
  max-width:1280px;
  .hero-text {
    white-space: pre-line;
    color:#fff;
    text-shadow:
      0px 0px 3px #32354d,
      0px 0px 3px #32354d,
      1px 1px 3px #32354d,
      0px 0px 10px #32354d,
      0px 0px 15px #303030,
      0px 0px 15px #000,
      0px 0px 20px #000;
  }
}
</style>
