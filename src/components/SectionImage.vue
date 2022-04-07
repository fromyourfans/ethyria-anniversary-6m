<template>
  <v-container class="section-grid">
    <v-row no-gutters class="mb-4">
      <v-col cols="12">
        <h1 class="yellow--text text--darken-3 text-center pa-0 ma-0">
          <img
            src="../assets/img/section-quilt.png" height="90"
            alt="Drawing Board" />
        </h1>
      </v-col>
    </v-row>
    <v-row no-gutters class="px-16">
      <v-col>
        <img src="@/assets/enna6m-quilt.png" class="quilt-img" alt="Art Quilt" />
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
.quilt-img {
  max-height:94vh;
  margin:auto;
  display:block;
}
</style>
