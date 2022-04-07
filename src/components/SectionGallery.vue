<template>
  <v-container class="section-grid section-box">
    <v-row no-gutters>
      <v-col cols="12">
        <h1 class="yellow--text text--darken-3 text-center pa-0 ma-0">
          <img
            src="../assets/img/section-gallery.png" height="60"
            alt="Art Gallery" />
        </h1>
        <!-- <h2 class="grey--text text-center pa-0 ma-0">
          Some Famillie celebrate 6 months and 200K through artworks
        </h2> -->
      </v-col>
    </v-row>
    <v-row no-gutters class="">
      <v-col>
        <div v-masonry="'gallery'" transition-duration="0.3s" item-selector=".card" stagger="0s">
          <div v-masonry-tile class="card">
            <a href="https://twitter.com/Nashiina2001/status/1489221995380486145" target="_blank">
              <img src="@/assets/art/6months-01-nashiina.jpeg" alt="@Nashiina2001" />
            </a>
            <div class="artist white--text text-center">Nashiina</div>
          </div>
          <div v-masonry-tile class="card">
            <a href="https://twitter.com/devildash27/status/1492514821711228931" target="_blank">
              <img src="@/assets/art/6months-02-devilkun.png" alt="@devildash27" />
            </a>
            <div class="artist white--text text-center">Devil-kun</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-03-nashiina.gif" alt="" />
            <div class="artist white--text text-center">Nashiina</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-04-nashiina.png" alt="" />
            <div class="artist white--text text-center">Nashiina</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-05-lostlittleone.png" alt="" />
            <div class="artist white--text text-center">lostlittle_one</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-06-leef.png" alt="" />
            <div class="artist white--text text-center">Leef</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-07-deskun.png" alt="" />
            <div class="artist white--text text-center">Deskun</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-08-kadabarvim.png" alt="" />
            <div class="artist white--text text-center">@Kadabar_VIM</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-09-nom.jpg" alt="" />
            <div class="artist white--text text-center">NOM</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-10-reignscarlet.jpg" alt="" />
            <div class="artist white--text text-center">Reign Scarlet</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-11-compressedrar.png" alt="" />
            <div class="artist white--text text-center">CompressedRar</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-12-stoveface.png" alt="" />
            <div class="artist white--text text-center">stoveface</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-13-lostlittleone.png" alt="" />
            <div class="artist white--text text-center">lostlittle_one</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-14-rafocado.png" alt="" />
            <div class="artist white--text text-center">rafocado</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-15-leef.png" alt="" />
            <div class="artist white--text text-center">Leef</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-16-deskun.png" alt="" />
            <div class="artist white--text text-center">Deskun</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-17-voldox.png" alt="" />
            <div class="artist white--text text-center">Voldox</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-18-mbisnotmybad.jpg" alt="" />
            <div class="artist white--text text-center">MBisnotmybad</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-19-reignscarlet.jpg" alt="" />
            <div class="artist white--text text-center">Reign Scarlet</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-20-butteredtoast.jpg" alt="" />
            <div class="artist white--text text-center">Buttered Toast</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-21-mafuyu.png" alt="" />
            <div class="artist white--text text-center">Mafuyu</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-22-aicia.png" alt="" />
            <div class="artist white--text text-center">Aicia</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-23-nashiina.png" alt="" />
            <div class="artist white--text text-center">Nashiina</div>
          </div>
          <div v-masonry-tile class="card">
            <a href="https://twitter.com/imoutoshepart/status/1511184234882363399" target="_blank">
              <img src="@/assets/art/6months-24-imoutoshepherd.png" alt="@imoutoshepart" />
            </a>
            <div class="artist white--text text-center">imoutoshepherd</div>
          </div>
           <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-25-shino.png" alt="" />
            <div class="artist white--text text-center">Shino</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-26-rafocado.png" alt="" />
            <div class="artist white--text text-center">rafocado</div>
          </div>
          <div v-masonry-tile class="card">
            <img src="@/assets/art/6months-27-pretzel.png" alt="" />
            <div class="artist white--text text-center">Pretzel</div>
          </div>
        </div>
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
  mounted() {
    this.$nextTick(() => {
      setTimeout(() => { this.$redrawVueMasonry('gallery'); }, 1000);
      setTimeout(() => { this.$redrawVueMasonry('gallery'); }, 5000);
    });
  },
};
</script>

<style lang="scss" scoped>
.card {
  background:#1a1a1a;
  position:relative;
  min-height:100px;
  width:24%;
  margin:10px 0.5%;
  padding:10px 10px 24px 10px;
  border:2px solid #0f0f0f;
  img {
    width:100%;
  }
  .artist {
    position:absolute;
    bottom:0;
    left:2px;
    right:2px;
    height:30px;
    line-height:30px;
    font-size:20px;
  }
}

@media only screen and (max-width: 1800px) {
  .card {
    width:32%;
    margin:10px 0.5%;
  }
}
@media only screen and (max-width: 1264px) {
  .card {
    width:48%;
    margin:10px 1%;
  }
}
@media only screen and (max-width: 700px) {
  .card {
    width:96%;
    margin:10px 2%;
  }
}
</style>
