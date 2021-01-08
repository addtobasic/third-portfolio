<template>
  <v-app dark>
    <v-card outlined id="main">
      <div>
        <v-card-title class="headline">
          <div v-if="error.statusCode === 404">
            {{ pageNotFound }}
          </div>
          <div v-else>
            {{ otherError }}
          </div>
        </v-card-title>
        <v-card-subtitle>
          <NuxtLink to="/">Go back to the top page.</NuxtLink>
        </v-card-subtitle>
      </div>
      <div class="animation" id="icon">
        <img class="img1" src="../static/img/genshi_line_animated.svg" alt="genshi_svg">
        <img class="img2" src="../static/img/icon.jpg" alt="icon_img">
      </div>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn
            outlined
            icon
            @click="reload"
        >
          <v-icon>mdi-reload</v-icon>
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>
<script>

export default {
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  methods: {
    reload:function(){
      var now = new Date().getTime();
      $('.img1').attr('src','https://smash-bros-stage-select-app.web.app/_nuxt/img/genshi_line_animated.9ce9c6d.svg'+'?'+''+now);

      // ↓localはこっち
      // $('.img1').attr('src','./_nuxt/static/img/genshi_line_animated.svg'+'?'+''+now);

      $(".img2").removeClass('animated');

      setTimeout(function() {
        $(".img2").addClass('animated');
      }, 1000);
    },
  },

  data () {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred',
    }
  },
  head () {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title
    }
  }
}
</script>
<style scoped>
  #main{
    top: 40%;
    left: 50%;
    -webkit-transform : translate(-50%,-50%);
    transform : translate(-50%,-50%);
  }

  #icon {
    background-color: white;
  }

  .animation {
    margin: auto;
    position: relative;
  }

  .animation img {
    width: 50%;
  }

  .animation .img1 {
    display: block;
    margin: 0 auto;
  }

  .animation .img2 {
    position: absolute;
    top: 0;
    left: 25%;
  }

.img2.animated {
  animation: fade-in 6s;
}

@keyframes fade-in {
    0% {
      opacity: 0;
    }

    12.5% {
      opacity: 0;
    }

    25.5% {
      opacity: 0;
    }
    37.5% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
}
  @keyframes animation {
    0% {
      opacity: 0;
    }

    12.5% {
      opacity: 0;
    }

    25.5% {
      opacity: 0;
    }
    37.5% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
  }

  .animation img {
    animation-name: animation;
    animation-duration: 7s;
    animation-iteration-count: 1;
  }

  .animation .img1 {
    animation-delay:5s;
  }

  @media screen and (min-width:0px) and ( max-width:600px){
    #icon{
      width:300px;
    }
  }

  @media screen and (min-width:600px) and ( max-width:767px){
    #icon{
      width:330px;
    }
  }

  @media screen and (min-width:767px) and ( max-width:960px){
    #icon{
      width:430px;
    }
  }

  @media screen and (min-width:960px) and ( max-width:1367px){
    #icon{
      width:500px;
    }
  }

  @media screen and (min-width:1367px) and ( max-width:2504px){
    #icon{
      width:500px;
    }
    #main{
      width: 900px;
    }
  }

  @media screen and (min-width:2504px) and ( max-width:3000px){
    #icon{
      width:544px;
    }
    #main{
      width: 1000px;
    }
  }
</style>
