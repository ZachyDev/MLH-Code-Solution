<template>
  <div class="form">
      <div class="box1">
          <h2>About Nipashe</h2>
          <img :src="require(`@/assets/${'dis.jpg'}`)" class="img-fluid" alt="statistics">
          <p><strong>Nipashe</strong> is a simple web app that gives you real time updates on the current COVID19 total reported cases,recoveries,deaths across the world.<br /> 
           <strong>Nipashe</strong> is a source you can trust.
        .</p>
      </div>
      <div class="box2">
          <h2>Fill the form below:</h2>
          <div class="form">
              <!-- country name -->
              <label for="country">Filter By Country Name</label>
              <input type="text" class="form-control" v-model="country" placeholder="Type Country Name"/>
              <!-- total infections -->
              <label for="country">Filter By County</label>
              <input type="text" class="form-control"  disabled placeholder="Type County Name"/>
              <label for="select-field">Advanced Search</label>
              <select class="form-control" disabled>
                  <option value="country">Country</option>
                  <option value="total">Total Infections</option>
              </select>
              <button class="btn btn-primary" @click="queryData">Submit</button>
          </div>
      </div>
   
  </div>
</template>

<script>
export default {
    name: "Form",
    data() {
        return{
            country: '',
            total: ''
        }
    },
    methods: {
        queryData() {
            this.$emit('queryString',this.country);
        }
    }
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
        .form {
            margin-top: 100px;
        }
        .box1 p{
            margin-top:10px;
            margin-left:-35px;
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
        .box1 img{
            width: 100%;
            margin-left:-35px;
        }
    }
    @media (max-width:768px) {
        .form{
            width:100%;
            max-width:100%;
            max-width: 100%;
            display:block;
            margin-top: 30px;
        }
        .box1{
            width:100%;
            max-width: 100%;
            margin-left:-40px;
            color:#333;
        }
        .box1 img{
            margin-top:10px;
            width: 100%;
            margin-left: -10px;
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
             width:80%;
             margin-left: -20px;
             border-radius:7px;
        }

    }
</style>