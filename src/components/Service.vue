<template>
  <div style="background: transparent; position: relative; z-index: 1">
    <div class="service-container grid bg-center bg-full bg-no-repeat px-100">
      <div class="service">
        <img src="../assets/images/ic-1.png" alt="" />
        <h3 class="font-heading text-pink-1">Premium Material</h3>
        <p class="font-body text-brown-1">
          Unsere hochwertige, vielfältige Premium-Materiale ermöglichen die
          beste Qualität und die schönste Optik für Ihre Nägel sowohl für den
          Alltag als auch für die besonderen Events.
        </p>
      </div>
      <!--Maniküre-->
      <div class="service">
        <img src="../assets/images/ic-2.png" alt="" />
        <h3 class="font-heading text-pink-1">Maniküre</h3>
        <p class="font-body text-brown-1">
          Von klassischer Maniküre bis zu den individuellen, einzigartigen
          Nageldesigns hegen und pflegen wir Ihre Hände.
        </p>
      </div>
      <!--Pediküre-->
      <div class="service">
        <img src="../assets/images/ic-3.png" alt="" />
        <h3 class="font-heading text-pink-1">Pediküre</h3>
        <p class="font-body text-brown-1">
          Lassen Sie uns Ihre Füße im harmonischen Einklang mit Ihren
          verschönerten Fingernägeln bringen.
        </p>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
// .service-container {
//   transform: translateY(-128%);
//   position: relative;
//   z-index: 0;
//   grid-template-columns: 1fr 1fr 1fr;
//   background-image: url('../assets/images/bg-intro.png');
//   .service {
//     transform: translateY(130%);
//   }
// }
.service-container {
  background-image: url('../assets/images/bg-intro.png');
  width: 100%;
  height: 410px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3rem;
  position: relative;
  transform: translateY(-1px);

  & > * {
    height: 360px !important;
  }
  .service {
    transform: translateY(calc(-17% + 1px));
    height: max-content;
    &:first-child {
      padding-left: 2rem;
    }
    &:nth-child(2) {
      padding: 0 1rem;
    }
    &:last-child {
      padding-right: 2rem;
    }
  }

  img {
    object-fit: contain;
    width: 100%;
    z-index: 3;
  }
}
</style>
