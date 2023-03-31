<template>
  <NavBar />
  <router-view />
</template>

<script setup lang="ts">
import NavBar from "@/components/panels/NavBar.vue";
</script>

<style lang="scss">
#app {
  font-family: Roboto, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  height: 100%;
}

html,
body {
  padding: 0px;
  margin: 0px;
  height: 100%;
  background: #2b2b2b;
}
</style>
