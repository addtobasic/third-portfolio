<template>
  <v-card light>
    <div id="aboutMain">
      <h1 id="title" align="center">About me</h1>
      <v-layout justify-center>
        <fade-in-component>
          <section>
            <v-card id="mainCard" class="d-inline-block mx-auto" elevation="8">
              <v-container>
                <v-row>
                  <v-col>
                    <div>
                      <v-card-title class="aboutText"
                        >面白いと思ったものと欲しいと思ったものと趣味に関するものを作るのがすきです</v-card-title
                      >
                      <v-list>
                        <v-list-item v-for="(item, i) in list" :key="i">
                          <v-list-item-icon>
                            <v-icon>{{ item.icon }}</v-icon>
                          </v-list-item-icon>
                          <v-list-item class="listText">{{
                            item.about
                          }}</v-list-item>
                        </v-list-item>
                      </v-list>
                    </div>
                  </v-col>
                </v-row>
              </v-container>
            </v-card>
          </section>
        </fade-in-component>
      </v-layout>
    </div>
  </v-card>
</template>

<script>
import FadeInComponent from '../components/FadeInComponent'
export default {
  components: {
    FadeInComponent,
  },
  data() {
    return {
      list: [
        {
          icon: 'mdi-school',
          about: '旭川工業高等専門学校 システム制御情報工学科 4年',
        },
        {
          icon: 'mdi-account-group',
          about: 'FuraIT, 旭川ゆるい勉強会, LOCAL学生部',
        },
        {
          icon: 'mdi-star',
          about: 'Twitter, アニメ鑑賞, ノベルゲーム, スマブラ',
        },
      ],
    }
  },
}
</script>
<style scoped>
/* タイトルにスペース */
#title {
  color: #35495e;
  padding: 30px 0px;
}

/* カードの下にテキスト */
#aboutMain {
  padding-bottom: 50px;
}

.aboutText {
  font-size: 18px;
}

@media screen and (min-width: 0px) and (max-width: 480px) {
  #mainCard {
    width: 340px;
  }

  .listText {
    font-size: 13px;
  }
}

@media screen and (min-width: 480px) and (max-width: 768px) {
  #mainCard {
    width: 420px;
  }

  .listText {
    font-size: 15px;
  }
}

@media screen and (min-width: 768px) and (max-width: 1024px) {
  #mainCard {
    width: 700px;
  }

  .aboutText {
    font-size: 20px;
  }

  .listText {
    font-size: 18px;
  }
}

@media screen and (min-width: 1024px) and (max-width: 1400px) {
  .aboutText {
    font-size: 20px;
  }

  .listText {
    font-size: 18px;
  }
}

@media screen and (min-width: 1400px) {
  .aboutText {
    font-size: 20px;
  }

  .listText {
    font-size: 18px;
  }
}
</style>
