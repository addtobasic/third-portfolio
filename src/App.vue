<template>
  <div id="app">
    <v-app>
      <v-navigation-drawer app v-model="drawer" clipped right>
        <v-container>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="title">
                Navigation
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-divider></v-divider>
          <v-list dense nav>
              <v-list-item-content>
                <v-list-item-title ><v-btn to='/' text>top</v-btn></v-list-item-title>
                <v-list-item-title><v-btn to='/Profile' text>profile</v-btn></v-list-item-title>
                <v-list-item-title><v-btn to='/Work' text>work</v-btn></v-list-item-title>
              </v-list-item-content>
          </v-list>
        </v-container>
      </v-navigation-drawer>
      <v-app-bar color="#48b883" dark app clipped-right style="height:60px;">
        <v-toolbar-title>Genshi's Portfolio</v-toolbar-title>
        <v-spacer></v-spacer>
        <Header v-if="true"></Header>
        <v-app-bar-nav-icon @click="drawer=!drawer" v-if="true"></v-app-bar-nav-icon>
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
  },
  data(){
    return{
        drawer: null
    }
  }
}
</script>
<style>

</style>
