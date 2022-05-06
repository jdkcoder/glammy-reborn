<template>
  <div class="footer-container relative">
    <div class="absolute top-0">
      <TitleRibbon title="Partners" />
    </div>
    <!--Partner Logos -->
    <div class="partner-logo grid items-center max-w-540 mx-auto">
      <div class="logo-item">
        <img src="../assets/images/partner_logo_1.png" alt="ADP" />
      </div>
      <div class="logo-item">
        <img src="../assets/images/partner_logo_2.png" alt="CitiBank" />
      </div>
      <div class="logo-item">
        <img src="../assets/images/partner_logo_3.png" alt="The Guardian" />
      </div>
      <div class="logo-item">
        <img src="../assets/images/partner_logo_4.png" alt="Adobe" />
      </div>
      <div class="logo-item">
        <img src="../assets/images/partner_logo_5.png" alt="Atlassian" />
      </div>
      <div class="logo-item">
        <img src="../assets/images/partner_logo_6.png" alt="Quizlet" />
      </div>
    </div>
    <!--Copyrights-->
    <div class="mx-auto">
      <h6 class="mb-0 font-heading font-normal uppercase text-16 text-brown-1">
        © Copyright Glammy Nails 2021
      </h6>
    </div>
  </div>
</template>
<script>
import TitleRibbon from './Ribbon/TitleRibbon.vue';
export default {
  name: 'Footer',
  components: {
    TitleRibbon,
  },
};
</script>
<style lang="scss" scoped>
.footer-container {
  background-image: url('../assets/images/bg-partners.png');
  .partner-logo {
    grid-template-columns: repeat(auto-fit, minmax(0, 1fr));
    gap: 40px;
  }
}
.absolute {
  z-index: 9;
}
</style>
