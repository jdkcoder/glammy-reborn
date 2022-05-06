<template>
  <div
    class="page-title items-center bg-center bg-full bg-no-repeat flex font-heading justify-center pb-10 relative text-align-center uppercase"
  >
    <h2>{{ title }}</h2>
  </div>
</template>
<script>
export default {
  name: 'TitleRibbon',
  props: ['title'],
};
</script>
<style lang="scss" scoped>
.page-title {
  background-image: url('/src/assets/images/bg-title.png');
  min-width: 306px;

  /*text*/
  padding: 1rem 2rem 1.5rem 2rem;
  color: rgba(107, 67, 59, 1);
  text-shadow: 2px 2px 0px rgb(0 0 0 / 25%);
  transform: translateY(-55%);
}
</style>
