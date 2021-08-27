<template>
  <v-card>
    <v-layout row>
      <v-flex v-for="(item, i) in items" :key="i" xl4 lg4 md6 sm12 xs12>
        <fade-in-component>
          <section>
            <div class="cardSpace">
              <v-container>
                <v-row dense>
                  <v-col id="colCenter">
                    <v-btn
                      id="productsBtn"
                      :href="item.url"
                      target="_blank"
                      rel="noreferrer"
                      style="text-transform: none"
                    >
                      <v-card
                        id="productsCard"
                        color="#37474f"
                        outlined
                        elevation="8"
                      >
                        <v-layout>
                          <v-img :src="item.image" :lazy-src="item.lazyImage">
                            <template v-slot:placeholder>
                              <v-row
                                class="fill-height ma-0"
                                align="center"
                                justify="center"
                              >
                                <v-progress-circular
                                  indeterminate
                                  color="grey lighten-5"
                                ></v-progress-circular>
                              </v-row>
                            </template>
                          </v-img>
                        </v-layout>
                        <v-card-title v-text="item.title"></v-card-title>
                        <v-card-subtitle>{{
                          item.description
                        }}</v-card-subtitle>
                      </v-card>
                    </v-btn>
                  </v-col>
                </v-row>
              </v-container>
            </div>
          </section>
        </fade-in-component>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
import FadeInComponent from '../components/FadeInComponent'
export default {
  name: 'About',

  components: {
    FadeInComponent,
  },

  data: () => ({
    items: [
      {
        title: 'My Portfolio Website',
        description: '今見てもらっているポートフォリオ',
        image: require('../assets/productsImages/portfolio.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/portfolio.png?raw=true',
        url: 'https://github.com/Genshi0916/Genshi0916.github.io',
      },
      {
        title: 'Stage Select App',
        description: 'スマブラの大会ステージ選択アプリ',
        image: require('../assets/productsImages/smash.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/smash.png?raw=true',
        url: 'https://smash-bros-stage-select-app.web.app/',
      },
      {
        title: 'When is the Deadline',
        description: '卒論提出や長期休み終了に使う邪悪なタイマー',
        image: require('../assets/productsImages/timer.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/timer.png?raw=true',
        url: 'https://genshi0916.github.io/when_is_the_deadline/#/',
      },
      {
        title: 'Twitter Yamero',
        description: 'Twitterをやめさせるフォームがでるchrome拡張機能',
        image: require('../assets/productsImages/twitter_yamero.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/twitter_yamero.png?raw=true',
        url: 'https://github.com/Genshi0916/Twitter_Yamero',
      },
      {
        title: 'Genshi Contribution Check',
        description: 'その日コミットしていなかったら煽られるtwitter bot',
        image: require('../assets/productsImages/contribution.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/contribution.png?raw=true',
        url: 'https://github.com/Genshi0916/genshi-contribution-check',
      },
      {
        title: 'Auto Add Hatena Blog Star',
        description: 'はてなブログの記事に任意個数starをつけてくれるアプリ',
        image: require('../assets/productsImages/hatena.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/hatena.png?raw=true',
        url: 'https://github.com/Genshi0916/auto-add-hatena-blog-star',
      },
      {
        title: 'BazUp!!',
        description: 'jigjpインターンで作った投稿した画像をバズらせるアプリ',
        image: require('../assets/productsImages/bazup.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/bazup.png?raw=true',
        url: 'https://github.com/Genshi0916/bazup',
      },
      {
        title: 'Auto Download Pixiv Images',
        description: 'pixivのブックマークをダウンロードしてくれるアプリ',
        image: require('../assets/productsImages/pixiv.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/pixiv.png?raw=true',
        url:
          'https://github.com/Genshi0916/auto-download-pixiv-bookmark-images',
      },
      {
        title: 'Auto Attendance Confirmation',
        description: '自動で出席確認のgoogle formに回答するアプリ',
        image: require('../assets/productsImages/form.png'),
        lazyImage:
          'https://github.com/Genshi0916/Genshi0916.github.io/blob/master/assets/productsImages/form.png?raw=true',
        url: 'https://github.com/Genshi0916/auto-attendance-confirmation',
      },
    ],
  }),
}
</script>

<style>
.cardSpace {
  padding: 30px 0px;
  /* padding-top:30px; */
}

#colCenter {
  text-align: center;
}

#productsCard {
  transition: opacity 0.2s ease-in-out;
  cursor: pointer;
}

#productsCard:hover {
  opacity: 0.7;
}

@media screen and (min-width: 0px) and (max-width: 480px) {
  #productsBtn {
    width: 340px;
    height: 280px;
  }

  #productsCard {
    width: 340px;
    height: 280px;
  }
}

@media screen and (min-width: 480px) and (max-width: 768px) {
  #productsBtn {
    width: 400px;
    height: 280px;
  }

  #productsCard {
    width: 400px;
    height: 280px;
  }
}

@media screen and (min-width: 768px) and (max-width: 1024px) {
  #productsBtn {
    width: 400px;
    height: 280px;
  }

  #productsCard {
    width: 400px;
    height: 280px;
  }
}

@media screen and (min-width: 1024px) and (max-width: 1400px) {
  #productsBtn {
    width: 400px;
    height: 280px;
  }

  #productsCard {
    width: 400px;
    height: 280px;
  }
}

@media screen and (min-width: 1400px) {
  #productsBtn {
    width: 400px;
    height: 280px;
  }

  #productsCard {
    width: 400px;
    height: 280px;
  }
}
</style>
