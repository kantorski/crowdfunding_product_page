<template>
  <div>
    <div class="card-body">
      <div class="logo-container">
        <img class="logo" src="../assets/logo-mastercraft.svg" alt="logo" />
      </div>
      <p class="brand-name">Mastercraft Bamboo Monitor Riser</p>
      <p class="brand-description">
        A beautiful & handcrafted monitor stand to reduce neck and eye strain.
      </p>
      <div class="options">
        <button class="project-deafult" @click="showModal = true">
          Back this project
        </button>
        <div>
          <img
            class="bookmark"
            src="../assets/icon-bookmark.svg"
            alt="bookmark"
          />
        </div>
      </div>
    </div>
    <div class="wrapper-inside" v-if="showModal">
      <div class="navbar">
        <p class="modal-title">Back this project</p>
        <img
          class="hamburger-menu"
          src="../assets/icon-close-modal.svg"
          @click="showModal = false"
        />
      </div>
      <p>
        Want to support us in bringing Mastercraft Bambo Monitor Riser out in
        the world
      </p>
      <div class="inside-card">
        <div class="product-bar">
          <input class="input-element" type="radio" name="option" />
          <p class="product-name product">Pledge with no reward</p>
        </div>
        <p class="product-descritption product">
          Choose to support us without a reward if you simply believe in our
          project. As a backer, you will be signed up to receive product updates
          via email.
        </p>
      </div>
      <div class="inside-card" :style="showPledge ? borderColor : null">
        <div class="product-bar">
          <input class="input-element" type="radio" name="option" @click="showPledge = true" />
          <div>
            <p class="product-name product">Bambo Stand</p>
            <p class="product-price product">Pledge $25 or more</p>
          </div>
        </div>
        <p class="product-descritption product">
          You get an ergonomic stand made of natural bamboo. You've helpe us
          launch our promotional campaign, and you’ll be added to a special
          Backer member list.
        </p>
        <div class="value-left">
          <p class="value product">101</p>
          <p class="left product">left</p>
        </div>
        <div class="pledge-wrapper" v-if="showPledge">
          <div class="line">
            <hr>
          </div>
          <p>Enter your pledge</p>
          <div class="pledge-select">
            <div class="captcha">
              <label for="pledge">$</label>
              <input class="pledge-value-input" type="text" id="pledge" />
            </div>
            <button>Continue</button>
          </div>
        </div>
      </div>
      <div class="inside-card">
        <div class="product-bar">
          <input class="input-element" type="radio" name="option" />
          <div>
            <p class="product-name product">Black Edition Stand</p>
            <p class="product-price product">Pledge $75 or more</p>
          </div>
        </div>
        <p class="product-descritption product">
          You get a Black Special Edition computer stand and a personal thank
          you. You’ll be added to our Backer member list. Shipping is included.
        </p>
        <div class="value-left">
          <p class="value product">64</p>
          <p class="left product">left</p>
        </div>
      </div>
      <div class="inside-card mahogany-card">
        <div class="product-bar">
          <input class="input-element" type="radio" name="option" />
          <div>
            <p class="product-name product">Mahogany Special Edition</p>
            <p class="product-price product">Pledge $200 or more</p>
          </div>
        </div>
        <p class="product-descritption product">
          You get two Special Edition Mahogany stands, a Backer T-Shirt, and a
          personal thank you. You’ll be added to our Backer member list.
          Shipping is included.
        </p>
        <div class="value-left">
          <p class="value product">0</p>
          <p class="left product">left</p>
        </div>
      </div>
    </div>
    <div class="modal-overlay" v-if="showModal"></div>
  </div>
</template>

<script>
export default {
  name: "FirstCardM",
  data: function () {
    return {
      showModal: false,
      showPledge: false,
      borderColor: {
        borderColor: 'hsl(176, 50%, 47%)',
        borderWidth: '2px'
      },
    };
  },
};
</script>

<style lang='scss' scoped>
$cayn-color: hsl(176, 50%, 47%);

.card-body {
  width: 86vw;
  max-width: 340px;
  margin: auto;
  background-color: white;
  border-radius: 8px;
  transform: translateY(-50px);
}
.logo-container {
  display: flex;
  align-items: center;
  justify-content: center;
  img {
    display: block;
    transform: translateY(-28px);
  }
}
.brand-name {
  margin: 0;
  padding: 0 40px;
  text-align: center;
  font-weight: bold;
  font-size: 20px;
}
.brand-description {
  text-align: center;
  color: grey;
  font-size: 15px;
  line-height: 0.75cm;
  padding: 0 20px;
}
.options {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  padding: 10px 20px 40px 20px;
}
.project-deafult {
  width: 75%;
  border-radius: 50px;
  border-style: none;
  background-color: $cayn-color;
  font-size: 15px;
  color: white;
  font-weight: bold;
  letter-spacing: 0.25px;
}

// MODAL

.wrapper-inside {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 80vw;
  padding: 25px 20px;
  border-radius: 10px;
  background-color: #fff;
  transform: translate(-50%, -15%);
  font-size: 15px;
  color: gray;
  line-height: 0.625cm;
  z-index: 10;
}

.navbar {
  display: flex;
  justify-content: space-between;

  .modal-title {
    margin: 0;
    font-size: 20px;
    font-weight: bold;
    text-align: center;
    color: black;
  }

  .hamburger-menu {
    width: 18px;
    height: 18px;
    z-index: 99;
  }
}

.product-card {
  width: 75vw;
  max-width: 282px;
  margin: 15px auto;
  font-size: 14px;
  line-height: 0.575cm;
  border: 1px solid grey;
  border-radius: 8px;
}

.inside-card {
  margin-top: 20px;
  padding: 25px 20px;
  border: 0.5px solid gray;
  border-radius: 10px;
}

.product {
  margin: 0;
  padding-bottom: 0;
}

.product-name {
  padding: 0;
  font-weight: bold;
  font-size: 15px;
  color: black;
}

.product-price {
  color: $cayn-color;
}

.product-descritption {
  padding: 20px 0;
}

.value-left {
  display: flex;
  align-items: center;
  padding: 5px 0;
  .value {
    color: black;
    font-weight: bold;
    font-size: 20px;
  }
  .left {
    padding-left: 10px;
  }
}

.product-bar {
  display: flex;
  align-items: center;

  .input-element[type="radio"] {
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    margin: 0;
    margin-right: 15px;
    padding: 4px;
    height: 24px;
    width: 24px;
    background-clip: content-box;
    border: 2px solid whitesmoke;
    border-radius: 50%;
  }

  .input-element[type="radio"]:checked {
    background-color: $cayn-color;
  }
}

.mahogany-card {
  opacity: 0.35;
}

.modal-overlay {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 9;
  background-color: rgba(0, 0, 0, 0.5);
}

.pledge-wrapper {
  p {
    text-align: center;
  }
  .pledge-select {
    display: flex;
    justify-content: space-around;
  }

  button {
    width: 30vw;
    height: 8vh;
    color: white;
    font-weight: bold;
    background-color: $cayn-color;
    border: none;
    border-radius: 25px;
  }
}

.pledge-value-input {
  width: 8vw;
  height: 7vh;
  color: black;
  font-size: 16px;
  font-weight: bold;
  background-color: white;
  border: none;
  border-radius: 25px;
}
.pledge-value-input:focus {
  outline: none;
}

.captcha {
  display: inline-block;
  height: 7vh;
  width: 23vw;
  padding-bottom: 0.2em;;
  background-color: white;
  border: 1px solid #A9A9A9;
  border-radius: 25px;
  label{
    padding-left: 20px;
    padding-right: 10px;
    color: grey;
    opacity: 0.45;
  }
}

.line{
  padding: 0;
}

</style>