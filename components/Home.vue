<template>
  <v-card
    :width="windowWidth"
    :height="windowHeight"
    style="background-color: #263238"
  >
    <div id="home">
      <div align="center">
        <div id="icon"></div>
      </div>
      <h1 id="nickName" align="center">Genshi</h1>
      <h2 id="name" align="center">Genki Kano</h2>
      <v-row justify="space-around">
        <a
          href="https://twitter.com/addtobasic"
          target="_blank"
          rel="noreferrer"
          ><v-icon>mdi-twitter</v-icon></a
        >
        <a href="https://github.com/addtobasic" target="_blank" rel="noreferrer"
          ><v-icon>mdi-github</v-icon></a
        >
        <a
          href="https://www.facebook.com/genki.kano.794"
          target="_blank"
          rel="noreferrer"
          ><v-icon>mdi-facebook</v-icon></a
        >
        <a
          href="https://www.instagram.com/addtobasic/"
          target="_blank"
          rel="noreferrer"
          ><v-icon>mdi-instagram</v-icon></a
        >
        <a href="https://qiita.com/addtobasic" target="_blank" rel="noreferrer"
          ><v-icon>mdi-pencil-box-multiple</v-icon></a
        >
      </v-row>
    </div>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    windowWidth: window.innerWidth,
    windowHeight: window.innerHeight,
  }),

  mounted() {
    window.addEventListener('resize', this.getWindowSize)
  },

  methods: {
    getWindowSize() {
      this.windowWidth = window.innerWidth
      this.windowHeight = window.innerHeight
    },
  },
}
</script>

<style scoped>
/* 上下中央揃え */
#home {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateY(-50%) translateX(-50%);
  -webkit-transform: translateY(-50%) translateX(-50%);
}

/* アイコンのクリック時にまばたき */
#icon {
  background-image: url('../assets/genshi.jpg');
  background-size: contain;
  height: 30vh;
  width: 30vh;
  border-radius: 50%;
  cursor: pointer;
}

#icon:active {
  background-image: url('../assets/mabataki.png');
}

/* 名前の下に少しスペース */
#name {
  padding-bottom: 18px;
}

/* aタグのデコレーションを消す */
a {
  text-decoration: none;
}
</style>
