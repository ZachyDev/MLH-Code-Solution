<template>
  <div class="home">
      <div class="home-content">
          <div class="col-sm-12">
              <h2>You can get it, I can get it!
            </h2></div>
          <img :src="require(`@/assets/${'team.jpg'}`)" class="img-fluid" alt="Home">
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
        font-family: 'Alata', sans-serif;
        font-family: 'Bree Serif', serif;
    }
    @media (max-width:760px) {
        .home h2{
            position: absolute;
            left: 5%;
            margin-top:100px;
            font-size: 29px;
            color:rgb(15, 18, 65);
        }
    }
    @media (min-width:760px) {
        .home h2{
            font-size: 70px;
            margin-left: -30px;
            margin-top:300px;
        }
    }
</style>
