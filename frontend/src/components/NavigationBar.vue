<template>
  <nav>
    <router-link to="/">Home</router-link>
    |
    <router-link to="/about">About</router-link>
  </nav>
</template>

<style scoped lang="scss">
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
