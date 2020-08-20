<template>
  <div class="header">
      <h1>Nipashe©</h1>
  </div>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style>
    .header{
        width:100%;
        max-width:100%;
        background:rgba(4,8,107,1);
        padding: 8px;
        color: #fff;
    }
    .header h1{
        font-family: 'Alata', sans-serif;
        font-family: 'Bree Serif', serif;
        font-size: 50px;
        display: swap;
    }
    @media(min-width: 768px) {
        .header {
            padding: 25px;
        }
    }
</style>