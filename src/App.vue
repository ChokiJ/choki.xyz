<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HomePage from "./components/HomePage.vue";
</script>

<template>
  <HomePage></HomePage>
</template>

<style>
@font-face {
    font-family: "Playfair Display Regular";
    src: local("Playfair Display Regular"),
        url(./fonts/PlayfairRomanVF.ttf);
}

@font-face {
    font-family: "Playfair Display Italic";
    src: local("Playfair Display Italic"),
        url(./fonts/PlayfairDisplay-Italic-VariableFont_wght.ttf);
}

#app {
    height: 100%;
    width: 100%;
}
</style>
