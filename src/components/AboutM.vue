<template>
  <div class="about-card">
    <p class="about-title">About this project</p>
    <p class="about-description">The Mastercraft Bamboo Monitor Riser is a sturdy and stylish platform that elevates your screen to a more comfortable viewing height. Placing your monitor at eye level has the potential to improve your posture and make you more comfortable while at work, helping you stay focused on the task at hand.</p>
    <p class="about-description">Featuring artisan craftsmanship, the simplicity of design creates extra desk space below your computer to allow notepads, pens, and USB sticks to be stored under the stand.</p>
    <BamboM/>
    <BlackEditionM/>
    <MahoganyM/>
  </div>
</template>

<script>
import BamboM from './BamboM.vue'
import BlackEditionM from './BlackEditionM.vue'
import MahoganyM from './MahoganyM.vue'

export default {
  name: 'AboutM',
  components: {
    BamboM,
    BlackEditionM,
    MahoganyM,
  }
}

</script>

<style lang='scss' scoped>
  .about-card{
    width: 86vw;
    max-width: 340px;
    margin: 0 auto;
    padding-bottom: 20px;
    background-color: white;
    border-radius: 8px;
  }
  .about-title{
    margin: 0;
    padding: 30px 20px 15px 20px;
    font-size: 18px;
    font-weight: bold;
  }
  .about-description{
    margin: 0;
    padding: 15px 20px;
    font-size: 14px;
    line-height: 0.575cm;
  }
</style>