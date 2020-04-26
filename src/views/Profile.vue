<template>
  <div>
    <p class="font-weight-black" align="center" id="profile">Profile</p>
    <v-layout justify-center>
      <v-card class="d-inline-block mx-auto" id="card">
        <v-container>
          <v-row>
            <v-col md="4" lg="3">
              <span id="nameGenki">Kano Genki</span>
              <v-img id="genki" src="../assets/genki.jpg"></v-img>
            </v-col>
            <v-col md="8" lg="9">
              <div>
                <p></p>
                <p>北海道の学生をしている加納源基といいます。留年しないように適度にさぼりつつプログラムを書いています。PC部に所属していて1,2年と、ぼんやり情報技術と触れ合っていしたが3年になってWebフロントエンド楽しいになってきてVueをさわさわしています。ひとおりさわってバックエンドにも興味が出てきたので次はDjangoかLaravelあたりをひとおりさわっていきたいと思っています。あと最近Atcorderを始めたので目標緑を目指しがんばります。
                </p>
                <p>VScode、npm、chrome、きのこの山、緑のたぬき、こしあん派です。</p>
                <v-list>
                  <v-list-item v-for="item in list" :key="item.icon">
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
    </v-layout>
  </div>
</template>
<script>
  export default{
    data(){
      return {
        list:[
          {icon:'fa-school',about:'旭川工業高等専門学校システム制御情報工学科3年'},
          {icon:'fa-users',about:'FuraIT,旭川ゆるい勉強会,LOCAL学生部'},
          {icon:'fa-star',about:'Twitter,アニメ鑑賞,ノベルゲーム,プログラミング'}
        ]
      }
    }
  }
</script>
<style scoped>
  #profile{
    color: #35495e;
  }

  #nameGenki{
    font-size: 23px;
    color: #35495e;
  }

  @media screen and (min-width:0px) and ( max-width:480px){
    #profile{
      margin-top:5px;
      font-size: 55px;

    }

    #card{
      width: 340px;
    }

    #genki{
      height: 300px;
      width: 340px;
    }
  }

  @media screen and (min-width:480px) and (max-width:768px){
    #profile{
      margin-top:30px;
      font-size: 55px;
    }

    #card{
      width: 420px;
    }

    #genki{
      height: 300px;
      width: 420px;
    }
  }

  @media screen and (min-width:768px) and ( max-width:1024px){
    #profile{
      margin-top:40px;
      font-size: 55px;
    }

    #card{
      width: 700px;
    }

    #genki{
      height: 300px;
      width: 300px;
    }
  }

  @media screen and (min-width:1024px) and ( max-width:1400px){
    #profile{
      margin-top:15px;
      font-size: 60px;
    }

    #card{
      height: 400px;
      width: 1000px;
    }

    #genki{
      height: 300px;
      width: 200px;
    }
  }

  @media screen and (min-width:1400px){
    #profile{
      margin-top:30px;
      margin-bottom:40px;
      font-size: 90px;
    }

    #genki{
      height: 300px;
      width: 300px;
    }
  }
</style>
