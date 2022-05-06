<template>
  <nav class="navbar-banner bg-no-repeat relative bg-center">
    <div class="navbar-menu relative">
      <div class="left-section flex">
        <div class="nav-item text-shadow uppercase">
          <a class="text-brown-1 hover:text-pink-1" href="">Home</a>
        </div>
        <div class="star">
          <img src="../assets/images/ic-star.png" alt="" />
        </div>
        <div class="nav-item text-brown-1 text-shadow uppercase">
          <a class="text-brown-1 hover:text-pink-1" href="">Standorte</a>
        </div>
      </div>

      <!--Logo -->
      <a href="#!" class="navbar-logo nav-item absolute">
        <img src="../assets/images/logo.png" alt="Navbar Logo" />
      </a>
      <!--End logo -->

      <div class="right-section flex">
        <div class="nav-item text-brown-1 text-shadow uppercase">
          <a class="text-brown-1 hover:text-pink-1" href="#booking"
            >Online Buchen</a
          >
        </div>
        <div class="star">
          <img src="../assets/images/ic-star.png" alt="" />
        </div>
        <div class="nav-item text-brown-1 text-shadow uppercase">
          <a class="text-brown-1 hover:text-pink-1" href="">Impressum</a>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  name: 'Navigation',
  methods: {
    goto(refName) {
      var element = this.refs[refName];
      element.scrollIntoview();
    },
  },
};
</script>
<style lang="scss" scoped>
a {
  text-decoration: none;
}
.navbar-banner {
  background-image: url('../assets/images/header.png');
  background-size: 100% 70%;
  height: 200px;
  width: 93%;
  position: fixed;
  left: 50%;
  transform: translateX(-50%);

  // height: 100%;
  //flex box
  //justify-content space arround
  z-index: 9999;
  .navbar-menu {
    display: flex;
    justify-content: space-around;
    align-items: center;
    list-style-type: none;
    height: 100%;

    & > * {
      display: flex;
      gap: 1.75rem;
    }
    .navbar-logo {
      height: 90%;
      width: auto;

      img {
        object-fit: contain;
      }
    }

    .left-section,
    .right-section {
      transform: translateY(-0.625rem);
      align-items: center;
      .star {
        img {
          height: 15px;
        }
      }
      .nav-item {
        font-family: 'Architecture', sans-serif;
        font-size: 32px;
        font-weight: 400;
      }
    }
  }
}
</style>
