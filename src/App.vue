<template>
  <div id="app">
    <v-app>
      <v-app-bar color="#48b883" app dark style="height:60px;">
        <v-toolbar-title>Genshi's Portfolio</v-toolbar-title>
        <v-spacer></v-spacer>
        <Header></Header>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
      </v-app-bar>
        <v-content>
          <router-view/>
        </v-content>
      <Footer></Footer>
    </v-app>
  </div>
</template>

<script>
import Header from './components/header'
import Footer from './components/footer'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
  }
};
</script>
<style>

</style>
