<template>
  <div>
    <p class="font-weight-black" align="center" id="work">Work</p>
    <v-layout justify-center>
      <v-card class="pa-6" id="card">
        <v-layout row wrap>
          <v-flex  v-for="(item,i) in list" :key="i">
            <v-card class="grey lighten-3 ma-4" height="400px">
              <v-container>
                <v-card-text>
                  <p align="center" id="title">{{item.title}}</p>
                  <v-layout justify-center>
                    <a @click="jumplink(link[i])"><img :src="image[i]" width="220px"></a>
                  </v-layout>
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
          {title:'FuraIT',comment:''},
          {title:'旭川ゆるい勉強会',comment:''},
          {title:'第3回 全国高専ビジネスコンテストby高専キャリア',comment:'チーム「よっぴー」MVT,サンケイエンジニアリング賞'},
          {title:'第30回高専プロコン',comment:'競技部門'},
          {title:'高専カンファin北海道',comment:'司会'},
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
      jumplink(link){
        window.open(link)
      }
    }
  }
</script>
<style scoped>
  #work{
    color: #35495e;
  }

  title{
    color: #35495e;
    font-size: 23px;
  }

  @media screen and (min-width:0px) and ( max-width:480px){
    #work{
      margin-top:5px;
      font-size: 55px;
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
