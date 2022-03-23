<template>
  <v-container class="section-grid">
    <v-row no-gutters class="mb-8">
      <v-col cols="12">
        <h1 class="yellow--text text--darken-3 text-center pa-0 ma-0">
          <img
            src="../assets/img/section-rewind.png" height="90"
            alt="Rewind" />
        </h1>
        <h2 class="grey--text text--darken-3 text-center pa-0 ma-0 white-glow">
          Looking back to the fun and amazing moments we had with Enna
        </h2>
      </v-col>
    </v-row>
    <v-row no-gutters class="rewind-item">
      <v-col>
        <div class="rewind-left text-right">
          <iframe title="feature-video" class="rewind-frame"
            width="640" height="360"
            src="https://www.youtube.com/embed/PKzGGJMCEmA"
            frameborder="0"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
            allowfullscreen>
          </iframe>
        </div>
        <div class="rewind-center">
          <div class="rewind-dot"></div>
        </div>
        <div class="rewind-right black--text">
          <div class="rewind-texts">
            <div class="card">
              <div class="card-name text-h6 pr-12 py-2">{{cards[0].name}}</div>
              <div class="card-text text-body-1 pr-4 pb-2">{{cards[0].message}}</div>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row no-gutters class="rewind-item">
      <v-col>
        <div class="rewind-left black--text text-right">
          <div class="rewind-texts">
            <div class="card">
              <div class="card-name text-h6 pr-12 py-2">{{cards[1].name}}</div>
              <div class="card-text text-body-1 pr-4 pb-2">{{cards[1].message}}</div>
            </div>
          </div>
        </div>
        <div class="rewind-center">
          <div class="rewind-dot"></div>
        </div>
        <div class="rewind-right text-left">
          <iframe title="feature-video" class="rewind-frame"
            width="640" height="360"
            src="https://www.youtube.com/embed/PKzGGJMCEmA"
            frameborder="0"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
            allowfullscreen>
          </iframe>
        </div>
      </v-col>
    </v-row>
    <v-row no-gutters class="rewind-item">
      <v-col>
        <div class="rewind-left text-right">
          <iframe title="feature-video" class="rewind-frame"
            width="640" height="360"
            src="https://www.youtube.com/embed/PKzGGJMCEmA"
            frameborder="0"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
            allowfullscreen>
          </iframe>
        </div>
        <div class="rewind-center">
          <div class="rewind-dot"></div>
        </div>
        <div class="rewind-right black--text">
          <div class="rewind-texts">
            <div class="card">
              <div class="card-name text-h6 pr-12 py-2">{{cards[2].name}}</div>
              <div class="card-text text-body-1 pr-4 pb-2">{{cards[2].message}}</div>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row no-gutters class="rewind-item">
      <v-col>
        <div class="rewind-left black--text text-right">
          <div class="rewind-texts">
            <div class="card">
              <div class="card-name text-h6 pr-12 py-2">{{cards[3].name}}</div>
              <div class="card-text text-body-1 pr-4 pb-2">{{cards[3].message}}</div>
            </div>
          </div>
        </div>
        <div class="rewind-center">
          <div class="rewind-dot"></div>
        </div>
        <div class="rewind-right text-left">
          <iframe title="feature-video" class="rewind-frame"
            width="640" height="360"
            src="https://www.youtube.com/embed/PKzGGJMCEmA"
            frameborder="0"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
            allowfullscreen>
          </iframe>
        </div>
      </v-col>
    </v-row>
    <v-row no-gutters class="rewind-item">
      <v-col>
        <div class="rewind-left text-right">
          <iframe title="feature-video" class="rewind-frame"
            width="640" height="360"
            src="https://www.youtube.com/embed/PKzGGJMCEmA"
            frameborder="0"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
            allowfullscreen>
          </iframe>
        </div>
        <div class="rewind-center">
          <div class="rewind-dot"></div>
        </div>
        <div class="rewind-right black--text">
          <div class="rewind-texts">
            <div class="card">
              <div class="card-name text-h6 pr-12 py-2">{{cards[4].name}}</div>
              <div class="card-text text-body-1 pr-4 pb-2">{{cards[4].message}}</div>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row no-gutters class="rewind-item">
      <v-col>
        <div class="rewind-left black--text text-right">
          <div class="rewind-texts">
            <div class="card">
              <div class="card-name text-h6 pr-12 py-2">{{cards[5].name}}</div>
              <div class="card-text text-body-1 pr-4 pb-2">{{cards[5].message}}</div>
            </div>
          </div>
        </div>
        <div class="rewind-center">
          <div class="rewind-dot"></div>
        </div>
        <div class="rewind-right text-left">
          <iframe title="feature-video" class="rewind-frame"
            width="640" height="360"
            src="https://www.youtube.com/embed/PKzGGJMCEmA"
            frameborder="0"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"
            allowfullscreen>
          </iframe>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: [],
  data: () => ({
    cards: null,
  }),
  mounted() {
    this.$root.$on('timelineCards', (cards) => {
      this.cards = cards;
      this.$nextTick(() => {
        this.$forceUpdate();
      });
    });
  },
};
</script>

<style lang="scss" scoped>
.rewind-item {
  position:relative;
  height:400px;
  .rewind-left {
    position:absolute;
    left:0;
    top:0;
    bottom:0;
    width:50%;
    padding-right:50px;
    .rewind-texts {
      right:50px;
    }
  }
  .rewind-center {
    width:0px;
    background:#fcc;
    position:absolute;
    left:50%;
    top:0;
    bottom:0;
    margin-left:-10px;
    border-left:4px solid #131313;
    .rewind-dot {
      width:30px;
      height:30px;
      background:#131313;
      border-radius:20px;
      border:4px solid #131313;
      position:absolute;
      top:50%;
      margin-left:-17px;
    }
  }
  .rewind-right{
    position:absolute;
    right:0;
    top:0;
    bottom:0;
    width:50%;
    padding-left:50px;
    .rewind-texts {
      left:50px;
    }
  }
  .rewind-frame {
    margin:20px;
    width:640px;
    height:360px;
    max-width:90%;
  }
  .rewind-texts {
    position:absolute;
    top:50%;
    transform:translateY(-50%);
  }
}

.card {
  position:relative;
  min-height:100px;
  width:100%;
  background:rgba(255, 255, 255, 0.3);
  padding:5px 20px;
  border-radius: 10px;
  .card-name {
    color:#343c75;
    font-weight:bold;
  }
  .card-text {
    white-space: pre-line;
    color:#000;
    max-height:280px;
    overflow-y:auto;
    overflow-x:hidden;
  }
}


</style>
