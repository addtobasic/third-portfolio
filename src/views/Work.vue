<template>
  <div>
    <p class="font-weight-black" align="center" id="work">Work</p>
    <v-layout justify-center>
      <v-card class="pa-6" id="card">
        <v-layout row wrap>
          <v-flex  v-for="(item,i) in list" :key="i">
            <v-card class="grey lighten-3 ma-4">
              <v-container>
                <v-card-text  id="center">
                  <v-col>
                  <p align="center" id="title">{{item.title}}</p>
                  <v-layout justify-center>
                    <a @click="jumpLink(link[i])">
                      <img :src="image[i]" id="cardImage">
                    </a>
                  </v-layout>
                  </v-col>
                  <v-col>
                    <p align="center" id="comment">{{item.comment}}</p>
                  </v-col>
                </v-card-text>
              </v-container>
            </v-card>
          </v-flex>
        </v-layout>
      </v-card>
    </v-layout>
  </div>
</template>
<script>
  export default{
    data:()=>({
        list:[
          {title:'FuraIT',comment:'僕が富良野市出身という縁もあって勉強会などでお手伝いさせてもらっています'},
          {title:'旭川ゆるい勉強会',comment:'旭川高専に通っているということもありまわりの友人たちも誘って勉強会のお手伝いをさせてもらっています'},
          {title:'第3回 全国高専ビジネスコンテストby高専キャリア',comment:'チーム「よっぴー」MVT,サンケイエンジニアリング賞を受賞しました'},
          {title:'第30回高専プロコン',comment:'競技部門に参加する予定だったが台風19号により移動部門敗退'},
          {title:'高専カンファin北海道',comment:'運営陣として参加し司会をしました'},
        ],
        image:[
          require("../assets/furait.jpg"),
          require("../assets/yurui.png"),
          require("../assets/bcon3.jpg"),
          require("../assets/procon30.jpg"),
          require("../assets/kosen_konf_hokkaido.png"),
        ],
        link:[
          "https://furait.connpass.com/",
          "https://asahikawa.connpass.com/",
          "https://third-kosen-bcon.peatix.com/view",
          "http://www.procon.gr.jp/?page_id=71201",
          "https://conf-hokkaido.connpass.com/event/122809/",
        ],
      }),
    methods:{
      jumpLink(link){
        window.open(link)
      }
    },

      props: {
    flat: Boolean,
    hover: Boolean,
    img: String,
    link: Boolean,
    loaderHeight: {
      type: [Number, String],
      default: 4,
    },
    outlined: Boolean,
    raised: Boolean,
    shaped: Boolean,
  },
  }
</script>
<style scoped>
  #work{
    color: #35495e;
  }

  #title{
    color: #35495e;
    font-size: 23px;
  }
  #cardImage{
    width:230px;
  }

  #cemter{
    justify-content: center;
  }

  @media screen and (min-width:0px) and ( max-width:480px){
    #work{
      margin-top:5px;
      font-size: 55px;
    }

    #title{
      color: #35495e;
      font-size: 20px;
  }

    #card{
      width: 340px;
    }
  }

  @media screen and (min-width:480px) and (max-width:768px){
    #work{
      margin-top:30px;
      font-size: 55px;
    }

    #card{
      width: 420px;
    }
  }

  @media screen and (min-width:768px) and ( max-width:1024px){
    #work{
      margin-top:40px;
      font-size: 55px;
    }

    #card{
      width: 700px;
    }
  }

  @media screen and (min-width:1024px) and ( max-width:1400px){
    #work{
      margin-top:15px;
      font-size: 60px;
    }

    #card{
      width: 1000px;
    }
  }

  @media screen and (min-width:1400px){
    #work{
      margin-top:30px;
      margin-bottom:40px;
      font-size: 90px;
    }

    #card{
      width: 1100px;
    }
  }
</style>
