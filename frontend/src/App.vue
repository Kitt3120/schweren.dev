<template>
  <LogoButton class="logo" />
  <NavigationPanel />
  <!----<NavBar />-->
  <router-view />
</template>

<script setup lang="ts">
import LogoButton from "./components/buttons/LogoButton.vue";
import NavigationPanel from "./components/panels/NavigationPanel.vue";
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto");

html,
body {
  padding: 0px;
  margin: 0px;
  color: #fff;
  background: #2b2b2b;
  font-family: Roboto, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.logo {
  position: fixed;
  display: inline;
  top: 1rem;
  left: 1rem;
  width: 0px;
  height: 0px;
  transform: scale(0.035);
}
</style>
