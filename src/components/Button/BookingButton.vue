<template>
  <a
    class="gold-btn bg-btn-gold bg-full bg-no-repeat bg-center font-heading px-40 py-17 text-brown-1 hover:text-white uppercase"
    href=""
    >{{ title }}</a
  >
</template>
<script>
export default {
  name: 'BookingButton',
  props: ['title'],
};
</script>
<style lang="scss">
.gold-btn {
  margin-top: 0.25rem;
  font-size:1.25rem;
  text-decoration: none;
}
</style>
