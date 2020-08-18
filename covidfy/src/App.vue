<template>
  <div class="container-fluid-sm">
      <div class="row">
          <div class="col-12">
              <Header />
              <Home />
              <Form />
          </div>
      </div>
  </div>
</template>

<script>
import Header from './components/Header';
import Home from './components/Home';
import Form from './components/Form';
export default {
    components: {
        Header,
        Home,
        Form
    }
}
</script>

<style>

</style>