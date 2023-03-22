<template>
  <button class="hamburger">
    <div class="row-1"></div>
    <div class="row-2"></div>
    <div class="row-3"></div>
  </button>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.hamburger {
  position: fixed;
  display: block;
  width: 50px;
  height: 50px;
  top: 10px;
  right: 10px;
  background: none;
  border: none;
  outline: none;
  appearance: none;
  cursor: pointer;
}

.hamburger div {
  content: "";
  display: block;
  width: 100%;
  height: 5px;
  background: gray;
  margin: 6px 0px;
  transition: 0.3s;
}

.hamburger.is-active {
  background: red;
}

.hamburger.is-active .row-1 {
  transform: rotate(45deg) translate(7px, 7px);
}

.hamburger-row-2.is-active {
  opacity: 0;
}

.hamburger-row-3.is-active {
  transform: rotate(-45deg) translate(7px, -7px);
}
</style>
