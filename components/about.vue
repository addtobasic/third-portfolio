<template>
  <v-card light>
    <div id="aboutMain">
      <h1 class="" align="center" id="title">About me</h1>
      <v-layout justify-center>
        <fade-in-component>
          <section>
            <v-card class="d-inline-block mx-auto" id="mainCard" elevation="8">
              <v-container>
                <v-row>
                  <v-col>
                    <div>
                      <p>Webらへんがすきです。面白いと思ったものをつくるのがすきです。</p>
                      <p>VScode、npm、chrome、きのこの山、緑のたぬき、こしあん派</p>
                      <v-list>
                        <v-list-item v-for="(item, i) in list" :key="i">
                          <v-list-item-icon>
                            <v-icon>{{item.icon}}</v-icon>
                          </v-list-item-icon>
                          <v-list-item-text>{{item.about}}</v-list-item-text>
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
  export default{
    components:{
      FadeInComponent,
    },
    data(){
      return {
        list:[
          {
            icon:'mdi-school',
            about:'旭川工業高等専門学校 システム制御情報工学科 3年'
          },
          {
            icon:'mdi-account-group',
            about:'FuraIT, 旭川ゆるい勉強会, LOCAL学生部'
          },
          {
            icon:'mdi-star',
            about:'Twitter, アニメ鑑賞, ノベルゲーム, スマブラ'
          }
        ]
      }
    }
  }
</script>
<style scoped>
  #title{
    color: #35495e;
    padding:30px 0px;
  }

  #aboutMain{
    padding-bottom: 30px;
  }


  @media screen and (min-width:0px) and ( max-width:480px){
    #card{
      width: 340px;
    }
  }

  @media screen and (min-width:480px) and (max-width:768px){
    #card{
      width: 420px;
    }
  }

  @media screen and (min-width:768px) and ( max-width:1024px){
    #card{
      width: 700px;
    }

    #genki{
      height: 300px;
      width: 300px;
    }
  }

  @media screen and (min-width:1024px) and ( max-width:1400px){
    #card{
      height: 400px;
      width: 1000px;
    }
  }

  @media screen and (min-width:1400px){

  }
</style>
