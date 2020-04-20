<template>
  <div id="app">
    <Header></Header>
    <div id="content">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Header from './components/header'
export default {
  name: 'App',
  components: {
    Header,
  }
};
</script>
