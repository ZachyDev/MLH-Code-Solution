<template>
  <div class="gallery">
      <h1> Best Practices</h1>
      <div class="card-group">
  <div class="card">
    <img :src="require(`@/assets/${'elb.jpg'}`)" class="card-img-top" alt="...">
    <div class="card-body">
      <h5 class="card-title">Cough to elbow</h5>
      <p class="card-text">Cover your nose and mouth with your bent elbow or a tissue when you cough or sneeze.</p>
      <p class="card-text"><small class="text-muted">You visited the page on {{timer}}</small></p>
    </div>
  </div>
  <div class="card">
    <img :src="require(`@/assets/${'sanit.jpg'}`)" class="card-img-top" alt="...">
    <div class="card-body">
      <h5 class="card-title">Sanitize</h5>
      <p class="card-text">If surfaces are dirty, they should be cleaned using a detergent or soap and water prior to disinfection.</p>
     <p class="card-text"><small class="text-muted">You visited the page on {{timer}}</small></p>
    </div>
  </div>
  <div class="card">
    <img :src="require(`@/assets/${'sha.jpg'}`)" class="card-img-top" alt="...">
    <div class="card-body">
      <h5 class="card-title">No Shaking</h5>
      <p class="card-text">No shaking of hands reduces chances of possible spread by contact.This is according to the Ministry guideline.</p>
        <p class="card-text"><small class="text-muted">You visited the page on {{timer}}</small></p>
    </div>
  </div>
</div>
  </div>
</template>

<script>
export default {
    name: "Prevention",
    computed: {
      timer() {
        return new Date().toLocaleString();
      }
    }
}
</script>

<style>
  .gallery{
    width: 100%;
    max-width: 100%;
    font-family: 'Alata', sans-serif;
    font-family: 'Bree Serif', serif;
  }
  @media (min-width:768px) {
    .gallery{
      margin-top:50px;
      width: 100%;
      max-width: 100%;
    }
    .gallery h1{
      display: flex;
      justify-content: center;
      margin-bottom: 20px;
    }
    .gallery img{
      margin-left:4px;
    }
    
  }
  @media (max-width:768px) {
    .gallery{
      margin-top:40px;
      width: 100%;
      max-width: 100%;
    }
    
  }
</style>