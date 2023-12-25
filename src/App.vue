<script setup lang="ts">
import Splash from './components/Splash.vue'
</script>

<template>
  <Splash></Splash>
</template>

<style>
* {
  margin: 0;
  padding: 0;
}

html,
body {
  height: 100vh;
  font-family: 'MS Sans Serif';
  overflow: hidden;
}

a {
  text-decoration: none;
  color: #fff;
  text-shadow: chartreuse;
  font-size: 1em;
  display: flex;
  align-items: center;
  flex-direction: column;
}

@font-face {
  font-family: 'MS Sans Serif', monospace;
  src: url('/font/ms_sans_serif_bold.woff');
}
</style>
