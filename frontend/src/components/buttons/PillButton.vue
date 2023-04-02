<template>
  <button class="pill">
    <slot />
  </button>
</template>

<style scoped lang="scss">
//Make button pill shaped
.pill {
  display: inline-block;
  background: linear-gradient(to left, #525252 50%, #bc956a 50%);
  background-size: 200% 100%;
  background-position: right bottom;
  color: #ffffff;
  border: none;
  border-radius: 16px;
  padding: 0.5rem 2rem;
  text-align: center;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.33s ease-out;
}

.pill:hover {
  background-position: left bottom;
}
</style>
