<script setup>
import PageLayout from './PageLayout.vue';
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
</script>

<template id="app">
  <PageLayout />
</template>

<style>
@import './assets/styles/app.scss';
@import '.\assets\styles\_base.scss';
/* Architecture font */
@font-face {
  font-family: 'Architecture';
  font-style: normal;
  font-display: auto;
  src: url('./assets/fonts/Architecture/ArchitecturePlain.woff') format('woff'),
    url('./assets/fonts/Architecture/ArchitecturePlain.woff2') format('woff2');
}
/* Noto Serif font */
@font-face {
  font-family: 'Noto Serif';
  font-style: normal;
  font-display: auto;
  src: url('./assets/fonts/NotoSerif-Regular.ttf') format('ttf');
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
