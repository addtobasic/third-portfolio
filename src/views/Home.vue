<template>
  <div>
    <div align="center">
      <div id="icon"></div>
    </div>
    <p class="font-weight-black" id="name" align="center">Genshi0916</p>
    <v-container>
      <v-layout justify-center>
        <v-btn v-for="site in sites" :key="site" class="mx-6" fab icon>
          <a v-bind:href="site.link" target="_blank">
            <v-avatar size="70">
              <img v-bind:src="site.icon" alt="avatar" id="radicon">
            </v-avatar>
          </a>
        </v-btn>
      </v-layout>
    </v-container>
  </div>
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
  }

  #icon:active{
    background-image: url("../assets/mabataki.png");
  }

  @media screen and (min-width:0px) and ( max-width:480px){
    #name{
      margin-top:5px;
      font-size: 55px;
    }

    #icon{
      margin-top:40px;
    }
  }

  @media screen and (min-width:480px) and (max-width:768px){
    #name{
      margin-top:30px;
      font-size: 55px;
    }

    #icon{
      margin-top:50px;
    }
  }

  @media screen and (min-width:768px) and ( max-width:1024px){
    #name{
      margin-top:40px;
      font-size: 55px;
    }

    #icon{
      margin-top:60px;
    }
  }

  @media screen and (min-width:1024px) and ( max-width:1400px){
    #name{
      margin-top:15px;
      font-size: 60px;
    }

    #icon{
      margin-top:50px;
    }
  }

  @media screen and (min-width:1400px){
    #name{
      margin-top:30px;
      margin-bottom:40px;
      font-size: 90px;
    }

    #icon{
      margin-top:70px;
    }
  }
</style>
