<template>
  <div>
    <p>Schweren.dev</p>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
// Let the p tag stick to the very left and let the HamburgerButton be on the very right of the navigation bar.
div {
  padding: 0px;
  width: 100%;
  height: 50px;
  margin: 0px;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.5), transparent 100%);
}

p {
  padding: 0px;
  margin: 0px;
  line-height: 50px;
  font-size: large;
  font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
  color: white;
  text-shadow: 0px 0px 5px black;
}

nav {
  padding: 30px;
}

a {
  color: #2c3e50;
  font-weight: normal;
  font-size: large;
  text-decoration: none;

  &.router-link-exact-active {
    color: #42b983;
    font-weight: bold;
  }
}
</style>
