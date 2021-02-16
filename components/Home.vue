<template>
  <v-card 
    :width="windowWidth"
    :height="windowHeight"
    style="background-color:#263238;"
  >
    <div id="home">
      <div align="center">
        <div id="icon"></div>
      </div>
      <h1 align="center" id="nickName">Genshi0916</h1>
      <h2 align="center" id="name" >Genki Kano</h2>
      <v-row justify="space-around">
        <a href="https://twitter.com/genshi0916" target="_blank" rel="noreferrer"><v-icon>mdi-twitter</v-icon></a>
        <a href="https://github.com/Genshi0916" target="_blank" rel="noreferrer"><v-icon>mdi-github</v-icon></a>
        <a href="https://www.facebook.com/genki.kano.794" target="_blank" rel="noreferrer"><v-icon>mdi-facebook</v-icon></a>
        <a href="https://www.instagram.com/genshi0916/" target="_blank" rel="noreferrer"><v-icon>mdi-instagram</v-icon></a>
        <a href="https://qiita.com/genshi0916" target="_blank" rel="noreferrer"><v-icon>mdi-blogger</v-icon></a>
      </v-row>
    </div>
  </v-card>
</template>

<script>
  export default {
    data:()=>({
      windowWidth: window.innerWidth,
      windowHeight: window.innerHeight,
    }),
    
    methods: {
      getWindowSize: function() {
        this.windowWidth = window.innerWidth;
        this.windowHeight = window.innerHeight;
      }
    },

    mounted() {
      window.addEventListener('resize', this.getWindowSize);
    },
  }
</script>

<style scoped>
/* 上下中央揃え */
  #home{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateY(-50%) translateX(-50%);
    -webkit-transform: translateY(-50%) translateX(-50%);
  }

/* アイコンのクリック時にまばたき */
  #icon{
    background-image: url("../assets/genshi.jpg");
    background-size: contain;
    height: 30vh;
    width: 30vh;
    border-radius: 50%;
    cursor: pointer;
  }

  #icon:active{
    background-image: url("../assets/mabataki.png");
  }

/* 名前の下に少しスペース */
  #name{
    padding-bottom: 18px;
  }

/* aタグのデコレーションを消す */
  a{
    text-decoration: none;
  }
</style>