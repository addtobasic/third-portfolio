<template>
  <v-app class="home">
    <div align="center">
      <div id="icon"></div>
    </div>
    <p class="display-3 font-weight-black" id="name" align="center">Kano Genki</p>
    <v-container>
      <v-layout justify-center>
        <v-btn v-for="site in sites" :key="site" class="mx-6" fab icon>
          <a v-bind:href="site.link">
            <v-avatar size="60">
              <img v-bind:src="site.icon" alt="avatar" />
            </v-avatar>
          </a>
        </v-btn>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
  export default {
    name: 'Home',
    components: {
    },
    data:()=>({
      sites:[
        {
          text:"twitter",
          link:"https://twitter.com/genshi0916",
          icon:require("../assets/twitter.png")
        },
        {
          text:"github",
          link:"https://github.com/Genshi0916",
          icon:require("../assets/github.png")
        },
        {
          text:"facebook",
          link:"https://www.facebook.com/genki.kano.794",
          icon:require("../assets/facebook.png")
        }
      ]
    })
  }
</script>
<style>
  #name{
    margin-top:20px;
    color: #35495e;
  }

  #icon{
    background-image: url("../assets/genshi.jpg");
    background-size: contain;
    height: 40vh;
    width: 40vh;
    background-repeat:  no-repeat;
    cursor: pointer;
    border-radius: 25%;
    margin-top: 20px;
  }

  #icon:active{
    background-image: url("../assets/mabataki.png");
  }
</style>
