<template>
  <v-container class="section-grid">
    <v-row no-gutters>
      <v-col cols="12">
        <h1 class="yellow--text text--darken-3 text-center pa-0 ma-0">
          <img
            src="../assets/img/section-messages.png" height="90"
            alt="Message Cards" />
        </h1>
        <h2 class="grey--text text--darken-3 text-center pa-0 ma-0 white-glow">
          Heartfelt messages from the Aloupeeps
        </h2>
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col class="pt-4">
        <div v-masonry="'bdaycards'" transition-duration="0.3s" item-selector=".card" stagger="0s">
          <div v-masonry-tile class="card card-style-3 card-tweet">
            <Tweet id="1511150040886173699"></Tweet>
          </div>
          <div
            v-masonry-tile
            :class="[ 'card', `card-style-${item.aloupeep}`]"
            v-for="(item, ix) in cards" :key="`card-${ix}`">
            <div class="card-name text-h6 pr-12 py-2">{{item.name}}</div>
            <div class="card-text text-body-1 pr-4 pb-2">{{item.message}}</div>
            <div class="card-aloupeep"></div>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import axios from 'axios';
import twemoji from 'twemoji';
import { Tweet } from 'vue-tweet-embed';

const FixedAloupeeps = {
  jetrico: 12,
  Zer0Pendragon6: 5,
};

export default {
  data: () => ({
    source: 'https://vtubertools.sfo3.digitaloceanspaces.com/tribute/enna6m.json',
    cards: [],
  }),
  methods: {
    shuffleCards() {
      for (let i = this.cards.length - 1; i > 0; i -= 1) {
        const j = Math.floor(Math.random() * (i + 1));
        // eslint-disable-next-line no-param-reassign
        [this.cards[i], this.cards[j]] = [this.cards[j], this.cards[i]];
      }
    },
    reSortCards() {
      this.cards = this.cards.sort((a, b) => {
        if (a.time > b.time) return 1;
        if (a.time < b.time) return -1;
        return 0;
      });
    },
  },
  mounted() {
    // Load data
    (async () => {
      const fetchSource = await axios.get(this.source).catch(() => null);
      const data = fetchSource && fetchSource.data ? fetchSource.data : {};
      this.cards = Object.values(data.messages)
        .map((card) => ({
          ...card,
          // aloupeep: 11,
          aloupeep: FixedAloupeeps[card.name] || Math.ceil(Math.random() * 12),
        }))
        .sort((a, b) => a.time - b.time);
      this.$nextTick(() => {
        twemoji.parse(document.body);
        this.$redrawVueMasonry('bdaycards');
        setTimeout(() => { this.$redrawVueMasonry('bdaycards'); }, 1200);
        setTimeout(() => { this.$redrawVueMasonry('bdaycards'); }, 3000);
        setTimeout(() => { this.$redrawVueMasonry('bdaycards'); }, 9000);
      });
    })();
  },
  components: {
    Tweet,
  },
};
</script>

<style lang="scss" scoped>
.card {
  // background:#b7bde7;
  background:rgba(183, 189, 231, 0.7);
  position:relative;
  padding:0px 10px 10px 10px;
  min-height:100px;
  width:24%;
  margin:10px 0.5%;
  border-radius:8px;
  // border:2px solid #0f0f0f;
  background-repeat: repeat-y;
  background-size: contain;
  &.card-tweet {
    background:none;
    padding:0px;
  }
  .card-aloupeep {
    width:100px;
    height:100px;
    position:absolute;
    top:-30px;
    right:-10px;
    // background-color:#f00;
    z-index:1;
    background-size:contain;
  }
  // fh, rich, wave
  &.card-style-1 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-01.png');
    }
  }
  &.card-style-2 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-02.png');
    }
  }
  &.card-style-3 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-art.png');
    }
  }
  &.card-style-4 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-cb.png');
    }
  }
  &.card-style-5 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-fh.png');
      top:-13px;
      z-index:3;
    }
  }
  &.card-style-6 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-ld.png');
    }
  }
  &.card-style-7 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-ms.png');
    }
  }
  &.card-style-8 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-rich.png');
      top:-9px;
      z-index:3;
    }
  }
  &.card-style-9 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-slp.png');
    }
  }
  &.card-style-10 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-td.png');
    }
  }
  &.card-style-11 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-wave.png');
      top:-17px;
      z-index:3;
    }
  }
  &.card-style-12 {
    .card-aloupeep {
      background-image:url('@/assets/img/aloupeeps/aloupeep-wiz.png');
    }
  }
  .card-name {
    color:#343c75;
    font-weight:bold;
    text-shadow:
      0px 0px 3px #fff,
      0px 0px 3px #fff,
      1px 1px 2px #fff;
  }
  .card-text {
    white-space: pre-line;
    font-weight:bold;
    padding:5px 10px;
    background-color:rgba(255, 255, 255, 0.7);
    border-radius:10px;
    position:relative;
    z-index:2;
    color:#000;
    text-shadow:
      0px 0px 3px #fff,
      0px 0px 3px #fff,
      0px 0px 15px #b7bde7;
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

<style lang="scss">
.card-text {
  img {
    height:1.4rem;
  }
}
</style>
