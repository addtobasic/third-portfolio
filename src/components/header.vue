<template>
    <v-layout wrap>
      <v-spacer></v-spacer>
      <v-btn to='/' text>top</v-btn>
      <v-btn
      v-for="item in items"
      :key="item.to"
      :to="item.to" text>{{item.to}}</v-btn>
    </v-layout>
    
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
  v-btn{
    color:black;
  }
</style>
