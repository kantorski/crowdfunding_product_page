<template>
  <div id="app">
    <HeroImageM/>
    <FirstCardM/>
    <SecondCardM/>
    <AboutM/>
  </div>
</template>

<script>
import HeroImageM from './components/HeroImageM.vue';
import FirstCardM from './components/FirstCardM.vue';
import SecondCardM from './components/SecondCardM.vue';
import AboutM from './components/AboutM.vue'

export default {
  name: 'App',
  components: {
    HeroImageM,
    FirstCardM,
    SecondCardM,
    AboutM,
  }
}
</script>

<style lang='scss'>
  @import url('https://fonts.googleapis.com/css2?family=Commissioner:wght@400;500;700&display=swap');

  body, html{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  #app{
    max-width: 375px;
    margin: 0 auto;
    font-family: Commissioner, sans-serif;
    background-color: whitesmoke;
    padding-bottom: 50px;
  }
</style>
