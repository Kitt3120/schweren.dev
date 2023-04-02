<template>
  <div class="navbar">
    <div class="logo" />

    <!-- <div class="links">
      <router-link to="/">Home</router-link>
      |
      <router-link to="/about">About</router-link>
    </div> -->
    <HamburgerButton id="button" />
  </div>
</template>

<script setup lang="ts">
import HamburgerButton from "@/components/buttons/HamburgerButton.vue";
</script>

<style scoped lang="scss">
.navbar {
  position: fixed;
  top: 0px;
  z-index: 1;
  height: 4rem;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: transparent;
}

.logo {
  width: 3rem;
  height: 3rem;
  margin: 0rem 2rem;
  background-color: #fff;
}

.links {
  position: relative;
  left: 0px;
  align-items: center;
  gap: 1rem;
}

#button {
  margin-right: 2rem;
}
</style>
