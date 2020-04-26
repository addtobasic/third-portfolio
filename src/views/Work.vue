<template>
  <div>
    <p class="font-weight-black" align="center" id="work">Work</p>
  </div>
</template>
<script>
  export default{
    data:()=>({
    })
  }
</script>
<style scoped>
  #work{
    color: #35495e;
  }

  @media screen and (min-width:0px) and ( max-width:480px){
    #work{
      margin-top:5px;
      font-size: 55px;

    }
  }

  @media screen and (min-width:480px) and (max-width:768px){
    #work{
      margin-top:30px;
      font-size: 55px;
    }
  }

  @media screen and (min-width:768px) and ( max-width:1024px){
    #work{
      margin-top:40px;
      font-size: 55px;
    }
  }

  @media screen and (min-width:1024px) and ( max-width:1400px){
    #work{
      margin-top:15px;
      font-size: 60px;
    }
  }

  @media screen and (min-width:1400px){
    #work{
      margin-top:30px;
      margin-bottom:40px;
      font-size: 90px;
    }
  }
</style>
