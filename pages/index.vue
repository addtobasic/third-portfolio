<template>
  <div>
    <Home/>
    <About/>
    <Products/>
    <Work/>
    <Contact/>
  </div>
</template>

<script>
  import Home from '../components/Home'
  import About from '../components/About'
  import Products from '../components/Products'
  import Work from '../components/Work'
  import Contact from '../components/Contact'

  export default {
    components:{
      Home,
      About,
      Products,
      Work,
      Contact
    },
  }
</script>
<style scoped>

</style>