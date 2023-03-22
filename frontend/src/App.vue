<template>
  <NavigationMenu />
  <HeaderBar />
  <router-view />
</template>

<script setup lang="ts">
import NavigationMenu from "@/components/buttons/HamburgerButton.vue";
import HeaderBar from "@/components/HeaderBar.vue";
</script>

<style lang="scss">
#app {
  font-family: Roboto, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  padding: 0px;
  margin: 0px;
}

html {
  padding: 0px;
  margin: 0px;
}
</style>
