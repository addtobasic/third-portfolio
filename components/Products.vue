<template>
  <v-card>
      <v-layout row>
        <v-flex
          xl4 lg4 md6 xs12
          v-for="(item, i) in items"
          :key="i"
        >
          <fade-in-component>
            <section>
              <v-container>
                <v-row dense>
                  <v-col id="colCenter">
                    <v-btn
                      width="400" 
                      height="300" 
                      :href="item.url" 
                      target="_blank" 
                      style="text-transform: none;"
                    >
                      <v-card
                        id="productsCard"
                        color="#37474f"
                        outlined
                        width="400"
                        height="300"
                        elevation="24"
                      >
                        <v-layout>
                          <v-img :src="item.image"></v-img>
                        </v-layout>
                        <v-card-title v-text="item.title"></v-card-title>
                        <v-card-subtitle>{{item.description}}</v-card-subtitle>
                      </v-card>
                    </v-btn>
                  </v-col>
                </v-row>
              </v-container>
            </section>
          </fade-in-component>
        </v-flex>
      </v-layout>
  </v-card>
</template>
<script>
  import FadeInComponent from '../components/FadeInComponent'
  export default{
    name:'about',
    components:{
      FadeInComponent
    },

    methods:{

    },

    data:()=>({
      items:[
        {
          title:"My Portfolio Website",
          description:"今見てもらっているポートフォリオ",
          image:require("../assets/productsImages/portfolio.png"),
          url:"https://github.com/Genshi0916/Genshi0916.github.io",
        },
        {
          title:"Stage Select App",
          description:"スマブラの大会ステージ選択アプリ",
          image:require("../assets/productsImages/smash.png"),
          url:"https://smash-bros-stage-select-app.web.app/",
        },
        {
          title:"When is the Deadline",
          description:"卒論提出や長期休み終了に使う邪悪なタイマー",
          image:require("../assets/productsImages/timer.png"),
          url:"https://genshi0916.github.io/when_is_the_deadline/#/",
        },
        {
          title:"Twitter Yamero",
          description:"Twitterをやめさせるフォームがでるchrome拡張機能",
          image:require("../assets/productsImages/twitter_yamero.png"),
          url:"https://github.com/Genshi0916/Twitter_Yamero",
        },
        {
          title:"Genshi Contribution Check",
          description:"その日コミットしていなかったら煽られるtwitter bot",
          image:require("../assets/productsImages/contribution.png"),
          url:"https://github.com/Genshi0916/genshi-contribution-check",
        },
        {
          title:"Auto Add Hatena Blog Star",
          description:"はてなブログの記事に任意個数starをつけてくれるアプリ",
          image:require("../assets/productsImages/hatena.png"),
          url:"https://github.com/Genshi0916/auto-add-hatena-blog-star",
        },
      ]
    })
  }
</script>
<style>

#colCenter{
  text-align: center;
}

#productsCard {
  transition: opacity .2s ease-in-out;
  cursor: pointer;
}

#productsCard:hover{
  opacity: 0.7;
}

  @media screen and (min-width:0px) and ( max-width:600px){
    #imageSize{
      height:180px;
      width:320px;
    }
  }

  @media screen and (min-width:600px) and ( max-width:960px){
    #imageSize{
      height:270px;
      width:480px;
    }
  }

  @media screen and (min-width:960px) and ( max-width:1367px){
    #imageSize{
      height:162px;
      width:288px;
    }
  }

  @media screen and (orientation: portrait) and (min-width:1023px) and ( max-width:1025px){
    #imageSize{
      height:162px;
      width:288px;
    }

    #ipad_pro_size{
      padding-top:200px;
      /*
        ipad proの縦の長さと ipadの横の長さが同じなのに涙を流して書いた部分です
        なにか良い実装方法があれば教えていただけると幸いです
       */
    }
  }

  @media screen and (min-width:1367px) and ( max-width:2504px){
    #imageSize{
      height:270px;
      width:480px;
    }
  }

  @media screen and (min-width:2504px) and ( max-width:3000px){
    #imageSize{
      height:306px;
      width:544px;
    }
  }
</style>
