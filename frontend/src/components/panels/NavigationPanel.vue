import HamburgerButton from '../buttons/HamburgerButton.vue';

<template>
  <HamburgerButton @click="($event) => (menuOpen = !menuOpen)" class="button" />
  <Transition name="slide">
    <div v-show="menuOpen" class="menu">
      <button>Test</button>
    </div>
  </Transition>
</template>

<script setup lang="ts">
import { Ref, ref } from "vue";
import HamburgerButton from "../buttons/HamburgerButton.vue";

const menuOpen: Ref<boolean> = ref(false);
</script>

<style scoped lang="scss">
.button {
  position: fixed;
  display: inline;
  top: 1rem;
  right: 1rem;
}

.menu {
  position: fixed;
  display: inline;
  top: 0;
  left: 80%;
  width: 20%;
  height: 100%;
  background: #313131;
  box-shadow: -5px 0 35px rgba(0, 0, 0, 0.5);
  z-index: 99;
}

.slide-enter-active,
.slide-leave-active {
  transition: all 0.75s ease-in-out;
}

.slide-enter-from,
.slide-leave-to {
  opacity: 0;
  box-shadow: none;
  left: 100%;
}
</style>
