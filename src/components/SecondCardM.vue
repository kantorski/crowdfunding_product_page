<template>
  <div class="card-body">
    <div class="values">
      <p class="value">{{money}}</p>
      <p class="value-info">of $100,00 backed</p>
      <hr>
    </div>
    <div class="values">
      <p class="value">{{totalBAckers}}</p>
      <p class="value-info">total backers</p>
      <hr>
    </div>
    <div class="values">
      <p class="value">{{daysLeft}}</p>
      <p class="value-info">days left</p>
    </div>
    <div class="progress">
      <progress class="progress-bar" value="70" max="100"></progress>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SecondCardM',
  data: function (){
    return {
      money: '$89,914',
      totalBAckers: '5,007',
      daysLeft: 56
    }
  },
}
</script>

<style lang='scss' scoped>

  $cayn-color: hsl(176, 50%, 47%);

  .card-body{
    width: 86vw;
    max-width: 340px;
    margin: 0 auto;
    background-color: white;
    border-radius: 8px;
    transform: translateY(-20px);
  }
  .values{
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
  }
  .value{
    margin: 0;
    margin-top: 30px;
    font-size: 36px;
    font-weight: bold;
  }
  .value-info{
    margin: 0;
    margin-top: 10px;
    color: grey;
  }
  .progress{
    display: flex;
    justify-content: center;
  }
  .progress-bar{
    width: 73vw;
    max-width: 300px;
    height: 13px;
    margin: 40px 0;
    background-color: $cayn-color;
    border-radius: 10px;
  }
  .progress-bar::-webkit-progress-bar{
    border-radius: 10px;
    background-color: #fff;
  }
  .progress-bar::-webkit-progress-value{
    background-color: $cayn-color;
    border-radius: 10px;
  }
  hr{
    width: 20vw;
    margin-top: 25px;
    margin-bottom: 0;
    color: grey;
  }
</style> 