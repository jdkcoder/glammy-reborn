<template>
  <div @click="scrollToTop" id="scroll-to-top" class="scroll-to-top pointer">
    <svg
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="74"
      height="74"
      viewBox="0 0 74 74"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
      data-v-2dedc691=""
    >
      <path
        d="M69 37C69 19.3269 54.6731 5 37 5C19.3269 5 5 19.3269 5 37C5 54.6731 19.3269 69 37 69C54.6731 69 69 54.6731 69 37Z"
        fill="#FEFFFF"
        data-v-2dedc691=""
      ></path>
      <path
        d="M71.5 37C71.5 17.9462 56.0538 2.5 37 2.5C17.9462 2.5 2.5 17.9462 2.5 37C2.5 56.0538 17.9462 71.5 37 71.5C56.0538 71.5 71.5 56.0538 71.5 37Z"
        stroke="#000000"
        stroke-opacity="0.1"
        stroke-width="5px"
        fill="none"
        data-v-2dedc691=""
      ></path>
      <path
        d="M34 29.8L41.2 37L34 44.2"
        stroke="#E6007E"
        stroke-width="4px"
        stroke-linecap="round"
        stroke-linejoin="round"
        fill="none"
        data-v-2dedc691=""
      ></path>
    </svg>
  </div>
</template>
<script>
export default {
  name: 'ScrollToTop',
  methods: {
    scrollToTop: function () {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    },
  },
};
</script>
<style lang="scss" scoped>
.scroll-to-top {
  transform: rotate(-90deg);
  position: fixed;
  z-index: 99;
  bottom: 20px;
  right: 20px;
}
</style>
