<template>
  <div class="home">
      <div class="home-content">
          <div class="col-sm-12">
              <h2>You can get it, I can get it!
            </h2></div>
          <img :src="require(`@/assets/${'home.jpg'}`)" class="img-fluid" alt="Home">
      </div>
  </div>
</template>

<script>
export default {
    name: "Home"
}
</script>

<style scoped>
    .home{
        overflow: hidden;
        width:100%;
        max-width: 100%;
    }
    .home img{
        width: 100%;
        max-width: 100%;
        height: auto;
        
    }
    .home h2{
        position: absolute;
        margin-top:400px;
        left: 33%;
        color:#fff;
        font-size: 50px;
    }
    @media (max-width:760px) {
        .home h2{
            position: absolute;
            left: 5%;
            margin-top:100px;
            font-size: 27px;
        }
    }
</style>
