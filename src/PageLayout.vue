<template>
  <div class="wrap">
    <!--Navbar -->
    <Navigation />
    <!--Slider -->
    <Slider />
    <!--Service-->
    <Service />
    <!--Booking-->
    <Booking ref="booking" />
    <!--Lopcation -->
    <Location />
    <!--Footer-->
    <!-- <Footer /> -->
    <!--Scroll to top button-->
    <ScrollToTop v-if="scrollpx > 800" />
  </div>
</template>
<script>
import Navigation from './components/Navigation.vue';
import Booking from './components/Booking.vue';
import Slider from './components/Slider.vue';
import Service from './components/Service.vue';
import Map from './components/Map/Map.vue';
import Footer from './components/Footer.vue';
import Location from './components/Location.vue';
import ScrollToTop from './components/Button/ScrollToTop.vue';
export default {
  name: 'PageLayout',
  components: {
    Navigation,
    Slider,
    Booking,
    Service,
    Map,
    Footer,
    Location,
    ScrollToTop,
  },
  data() {
    return {
      scrollpx: 0,
    };
  },
  methods: {
    // Show scroll to top button when after scrolling down n pixels
    handleScroll() {
      this.scrollpx = window.scrollY;
    },
  },
  mounted: function () {
    document.body.addEventListener('scroll', this.showScrollToTop);
  },
  created() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
};
</script>
<style lang="scss">
.wrap {
  background-image: url('./assets/images/body_bg.png');
  background-size: 2%;
  background-repeat: repeat;
  padding: 5px 130px;
  position: relative;
  height: 100%;
  min-height: 100vh;
}
</style>
