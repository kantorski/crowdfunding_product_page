<template>
  <div class="hero-image">
    <div class="navbar">
      <p class="title">crowdfund</p>
      <img class="hamburger-menu" src="../assets/icon-hamburger.svg">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeroImageM',
}
</script>

<style lang='scss' scoped>
  .hero-image{
    width: 100%;
    height: 270px;
    background-image: linear-gradient(rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.25)), url('../assets/image-hero-mobile.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
  }
  .navbar{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 15px 20px;
    color: white;
    font-weight: bold;
  }
  .hamburger-menu{
    padding-top: 6px;
    color: white;
    height: 15px;
    width: 16px;
    text-align: center;
  }
  .title{
    margin: 0;
    font-size: 24px;
    text-align: justify;
  }
</style>