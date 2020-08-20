<template>
  <div class="container-fluid-sm" id="app">
      <div class="row">
          <div class="col-12">
              <Header />
              <Home />
              <Form @queryString="queryString"/>
              <Stats :statistics="statistics"/>
              <Prevention />
              <Footer />
          </div>
      </div>
  </div>
</template>

<script>
import Header from './components/Header';
import Home from './components/Home';
import Form from './components/Form';
import Stats from './components/Stats';
import Prevention from './components/Prevention';
import Footer from "./components/Footer";
import axios from 'axios';
export default {
    components: {
        Header,
        Home,
        Form,
        Stats,
        Prevention,
        Footer
    },
    data() {
        return {
            statistics: []
        }
    },
    methods: {
        queryString(country) {
            console.log(country)
                axios.get(`https://covid-19-coronavirus-statistics.p.rapidapi.com/v1/total?country=${country}`, {
                "method": "GET",
                "headers": {
                "x-rapidapi-host": "covid-19-coronavirus-statistics.p.rapidapi.com",
                "x-rapidapi-key": "6a7f8e0053mshb9abe890d64e508p192e05jsn7b2ee60ecc40"
                }
                })
                .then(response => {
                    this.statistics = response.data;
                    // console.log(response.data)
                })
                .catch(err => {
                    alert('Failed to fetch data',err);
                });
        }
    }
}
</script>

<style scoped>
    #app{
        width: 100%;
        max-width: 100%;
        overflow: hidden;
    }
</style>