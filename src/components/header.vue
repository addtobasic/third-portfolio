<template>
  <v-toolbar
  dense
  color="black"
  ripple
  style="height:70px">
    <v-layout justify-center fill-height>
      <v-toolbar-items class="hidden-sm-and-down">
        <router-link to='/' class="link">
          <v-btn
          flat
          color="black"
          style="height:70px;
          width:100px;
          font-weight:bold;">
            top
          </v-btn>
        </router-link>
        <router-link
          class="link"
          v-for="item in items"
          :key="item.to"
          :to="item.to"
        >
          <v-btn
          flat
          color="black"
          style="height:70px;
          width:100px;
          font-weight:bold;">
          {{item.to}}
          </v-btn>
        </router-link>
      </v-toolbar-items>
    </v-layout>
  </v-toolbar>
</template>
<script>
  export default{
    name:'header',
    data:()=>({
      items:[
        {to:'Profile'},
        {to:'Work'}
      ]
    })
  }
</script>
<style>
.link{
  text-decoration:none;
}
</style>
