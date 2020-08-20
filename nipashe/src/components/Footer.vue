<template>
 <div class="footer">
     <!-- Footer -->
<footer class="page-footer font-small special-color-dark pt-4">

  <!-- Footer Elements -->
  <div class="container">
    <!-- Social buttons -->
    <ul class="list-unstyled list-inline text-center">
      <li class="list-inline-item">
          <a href="https://twitter.com/tiz_dev" target="_blank"><i class="fab fa-twitter"></i></a>
      </li>
      <li class="list-inline-item">
        <a href="https://github.com/ZachyDev" target="_blank"><i class="fab fa-github"></i></a>
      </li>
      <li class="list-inline-item">
       <a href="https://www.linkedin.com/in/zachydev/" target="_blank"><i class="fab fa-linkedin-in"></i></a>
      </li>
    </ul>
    <!-- Social buttons -->

  </div>
  <!-- Footer Elements -->

  <!-- Copyright -->
  <div class="footer-copyright text-center py-3">© {{ footerYear }} Copyright:
    <a href="https://codewithzachy.netlify.com/" target="_blank">This is Zachy #TIZ</a>
  </div>
  <!-- Copyright -->

</footer>
<!-- Footer -->
 </div>
</template>

<script>
export default {
    name: "footer",
    computed:{
        footerYear() {
            return new Date().getFullYear();
        }
    }
}
</script>

<style>

</style>