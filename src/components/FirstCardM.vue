<template>
  <div class="card-body">
    <div class="logo-container">
      <img class="logo" src="../assets/logo-mastercraft.svg" alt="logo">
    </div>
    <p class="brand-name">Mastercraft Bamboo Monitor Riser </p>
    <p class='brand-description'>A beautiful & handcrafted monitor stand to reduce neck and eye strain.</p>
    <div class="options">
      <button class="project-deafult">Back this project</button>
      <div>
        <img class='bookmark' src="../assets/icon-bookmark.svg" alt="bookmark">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FirstCardM'
}
</script>

<style lang='scss' scoped>

  $cayn-color: hsl(176, 50%, 47%);

  .card-body{
    width: 86vw;
    max-width: 340px;
    margin: auto;
    background-color: white;
    border-radius: 8px;
    transform: translateY(-50px);
  }
  .logo-container{
    display: flex;
    align-items: center;
    justify-content: center;
    img{
      display: block;
      transform: translateY(-28px);
    }
  }
  .brand-name{
    margin: 0;
    padding: 0 40px;
    text-align: center;
    font-weight: bold;
    font-size: 20px;
  }
  .brand-description{
    text-align: center;
    color: grey;
    font-size: 15px;
    line-height: 0.75cm;
    padding: 0 20px;
  }
  .options{
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    padding: 10px 20px 40px 20px;
  }
  .project-deafult{
    width: 75%;
    border-radius: 50px;
    border-style: none;
    background-color: $cayn-color;
    font-size: 15px;
    color: white;
    font-weight: bold;
    letter-spacing: 0.25px;
  }
</style>