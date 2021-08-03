<template>
  <div class="wrapper">
    <div class="hero-image">
      <div class="navbar">
        <p class="title">crowdfund</p>
        <img
          class="hamburger-menu"
          src="../assets/icon-hamburger.svg"
          @click="showModal = true"
          v-if="!showModal"
        />
        <img
          class="hamburger-menu"
          src="../assets/icon-close-menu.svg"
          @click="showModal = false"
          v-if="showModal"
        />
      </div>
      <div class="menu" v-if="showModal">
        <p>About</p>
        <hr />
        <p>Discovery</p>
        <hr />
        <p>Get Started</p>
      </div>
    </div>
    <div class="modal-overlay" v-if="showModal"></div>
  </div>
</template>

<script>
export default {
  name: "HeroImageM",
  data: function () {
    return {
      showModal: false,
    };
  },
};
</script>

<style lang='scss' scoped>
.hero-image {
  width: 100%;
  height: 270px;
  background-image: linear-gradient(rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.25)),
    url("../assets/image-hero-mobile.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.navbar {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 15px 20px;
  color: white;
  font-weight: bold;
}
.hamburger-menu {
  padding-top: 6px;
  color: white;
  height: 15px;
  width: 16px;
  text-align: center;
  z-index: 11;
}
.title {
  margin: 0;
  font-size: 24px;
  text-align: justify;
}
.menu {
  position: absolute;
  top: 70%;
  left: 50%;
  width: 80vw;
  background-color: #fff;
  border-radius: 10px;
  transform: translate(-50%, -50%);
  z-index: 10;
  p {
    padding: 7px 20px;
    font-size: 16px;
    font-weight: bold;
  }
  hr {
    height: 0.1px;
    background-color: whitesmoke;
  }
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
</style>