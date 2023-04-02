<template>
  <button @click="onClick">
    <div class="row-1" :class="{ active: isActive }"></div>
    <div class="row-2" :class="{ active: isActive }"></div>
    <div class="row-3" :class="{ active: isActive }"></div>
  </button>
</template>

<script setup lang="ts">
import { Ref, ref } from "vue";

const isActive: Ref<boolean> = ref(false);

const onClick = () => {
  isActive.value = !isActive.value;
};
</script>

<style scoped lang="scss">
button {
  display: block;
  width: 50px;
  height: 50px;
  z-index: 100;

  cursor: pointer;
  background: none;
  border: none;
  outline: none;
  appearance: none;
}

button div {
  display: block;
  width: 100%;
  height: 5px;
  margin: 6px 0px;
  background: gray;

  content: "";
}

.row-1 {
  transition: 0.5s ease-in-out;
}

.row-2 {
  transition: 0.5s ease-in-out 0.25s;
}
.row-3 {
  transition: 0.5s ease-in-out;
}

.row-1.active {
  transition: 0.5s ease-in-out 0.25s;
  transform: rotate(25deg) translate(2px, 2px);
  border-radius: 33%;
}

.row-2.active {
  transition: 0.5s ease-in-out;
  opacity: 0;
  transform: translateX(-10px);
}

.row-3.active {
  transition: 0.5s ease-in-out 0.25s;
  transform: rotate(-25deg) translate(2px, -2px);
  border-radius: 33%;
}
</style>
