<script setup lang="ts">
import Splash from './components/Splash.vue'

</script>

<template>
  <div class="page-container">
    <Splash></Splash>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
}

html,
body {
  overflow: hidden;
  height: 100svh;
  background: hsl(287, 94%, 7%);
}

.page-container {
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  height: 100svh;
  background-color: #000;
}
</style>
