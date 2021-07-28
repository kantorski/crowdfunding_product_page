<template>
  <div class="product-card">
    <div class="inside-card">
      <p class="product-name product">Bambo Stand</p>
      <p class="product-price product">Pledge ${{ pledge }} or more</p>
      <p class="product-descritption product">
        You get an ergonomic stand made of natural bamboo. You've helped us
        launch our promotional campaign, and you’ll be added to a special Backer
        member list.
      </p>
      <div class="value-left">
        <p class="value product">{{ valueLeft }}</p>
        <p class="left product">left</p>
      </div>
      <button id="modal-open" @click="showModal = true">Select Reward</button>
    </div>
    <transition name="fade" appear>
      <div class="modal-overlay" v-if="showModal" @click="showModal = false"></div>
    </transition>
    <transition name="slide" appear>
      <div class="modal" v-if="showModal" @click="showModal = false">
        <img src="../assets/icon-check.svg" alt="" />
        <p class="modal-title">Thanks for your support!</p>
        <p class="modal-description">
          Your pledge brings us one step closer to sharing Mastercraft Bamboo
          Monitor Riser worldwide. You will get an emial once your campaign is
          completed
        </p>
        <button class="modal-close">Got it!</button>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "BamboM",
  data: function () {
    return {
      valueLeft: 101,
      pledge: 25,
      showModal: true,
    };
  },
};
</script>

<style lang='scss' scoped>
$cayn-color: hsl(176, 50%, 47%);

.product-card {
  width: 75vw;
  margin: 15px auto;
  font-size: 14px;
  line-height: 0.575cm;
  border: 1px solid grey;
  border-radius: 8px;
}

.inside-card {
  margin: 20px;
}

.product {
  margin: 0;
}

.product-name {
  font-weight: bold;
  font-size: 15px;
  padding-bottom: 5px;
}

.product-price {
  color: $cayn-color;
}

.product-descritption {
  padding: 20px 0;
}

.value-left {
  display: flex;
  padding: 5px 0;
  .value {
    font-size: 32px;
    font-weight: bold;
  }
  .left {
    padding-left: 10px;
    font-weight: bold;
  }
}

button {
  width: 42vw;
  height: 48px;
  margin-top: 25px;
  border: none;
  border-radius: 50px;
  background-color: $cayn-color;
  color: white;
  font-weight: bold;
}

.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  width: 90vw;
  border: 0.5px solid black;
  border-radius: 15px;
  transform: translate(-50%, -50%);
  background-color: #fff;
  z-index: 99;

  .modal-title {
    text-align: center;
    font-weight: bold;
    font-size: 18px;
  }
  .modal-description {
    text-align: center;
    padding: 0 30px;
  }
  .modal-close {
    position: relative;
    top: 50%;
    left: 50%;
    width: 30vw;
    margin-bottom: 40px;
    transform: translate(-50%, 0);
  }
}

img {
  position: relative;
  top: 50%;
  left: 50%;
  width: 60px;
  height: 60px;
  margin-top: 30px;
  transform: translate(-50%, 0);
}

.modal-overlay {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 98;
  background-color: rgba(0, 0, 0, 0.5);
}
</style>