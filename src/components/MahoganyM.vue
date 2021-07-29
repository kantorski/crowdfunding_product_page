<template>
  <div class="product-card">
    <div class="inside-card">
      <p class="product-name product">Mahogany Special Edition</p>
      <p class="product-price product">Pledge ${{ pledge }} or more</p>
      <p class="product-descritption product">
        You get two Special Edition Mahogany stands, a Backer T-Shirt, and a
        personal thank you. You’ll be added to our Backer member list. Shipping
        is included.
      </p>
      <div class="value-left">
        <p class="value product">{{ valueLeft }}</p>
        <p class="left product">left</p>
      </div>
      <button>Out of Stock</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "MahoganyM",
  data: function () {
    return {
      valueLeft: 0,
      pledge: 200,
    };
  },
};
</script>

<style lang='scss' scoped>

$cayn-color: hsl(176, 50%, 47%);

.product-card {
  width: 75vw;
  max-width: 282px;
  margin: 15px auto;
  opacity: 0.35;
  font-size: 14px;
  line-height: 0.575cm;
  border: 1px solid grey;
  border-radius: 8px;
  // padding-bottom: 30px;
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
  background-color: grey;
  color: white;
  font-weight: bold;
}
</style>