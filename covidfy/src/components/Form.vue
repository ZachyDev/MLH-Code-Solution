<template>
  <div class="form">
      <div class="box1">
          <h2>How to Use</h2>
          <img :src="require(`@/assets/${'home.jpg'}`)" class="img-fluid" alt="statistics">
          <p>CovidFy is a simple web app to check real-time updates on the current COVID-19 statistics across all regions
            Covidfy utilizes COVID-19 statistics API that provides various endpoints such us country,region,total infections and so on.
        .</p>
      </div>
      <div class="box2">
          <h2>Fill the form below:</h2>
          <div class="form">
              <!-- country name -->
              <label for="country">Filter By Country Name</label>
              <input type="text" class="form-control"  placeholder="Type Country Name"/>
              <!-- total infections -->
              <label for="country">Filter By County</label>
              <input type="text" class="form-control"  placeholder="Type County Name"/>
              <label for="select-field">Advanced Search</label>
              <select class="form-control">
                  <option value="country">Country</option>
                  <option value="county">County</option>
                  <option value="total">Total Infections</option>
              </select>
              <button class="btn btn-success">Submit</button>
          </div>
      </div>
   
  </div>
</template>

<script>
export default {
    name: "Form"
}
</script>

<style>
    .form{
        display: grid;
        grid-template-columns: 1.5fr 2fr;
        margin: 50px;
        font-family: 'Alata', sans-serif;
        font-family: 'Bree Serif', serif;
    }
    .box2{
        margin-left: 100px;
    }
    @media (min-width:768px) {
        .box1 p{
            margin-top:10px;
        }
         .box2 input[type="text"],label{
            width:80%;
            max-width:100%;
            margin-top:10px;
            margin-left:-20px;
        }
        .box2 select{
            width:80%;
            max-width:100%;
            margin-top:10px;
            margin-left:-20px;
        }
        .box2 button{
             margin-top:20px;
             width:65%;
             border-radius:7px;
        }
    }
    @media (max-width:768px) {
        .form{
            width:100%;
            max-width:100%;
            max-width: 100%;
            display:block;
        }
        .box1{
            width:100%;
            max-width: 100%;
            margin-left:-40px;
            color:#333;
        }
        .box1 img{
            margin-top:10px;
        }
        .box1 p{
            margin-top:10px;
        }

        .box2 {
            width:100%;
            max-width: 100%;
            margin-left:-40px;
            margin-top:30px;
        }
        .box2 input[type="text"],label{
            width:80%;
            max-width:100%;
            margin-top:10px;
            margin-left:-20px;
        }
        .box2 select{
            width:80%;
            max-width:100%;
            margin-top:10px;
            margin-left:-20px;
        }
        .box2 button{
             margin-top:20px;
             width:65%;
             border-radius:7px;
        }

    }
</style>