<template>
  <button :class="{ active: isActive }" @click="onClick">
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

  cursor: pointer;
  background: none;
  border: none;
  outline: none;
  appearance: none;

  transition: 0.5s ease-in-out;
}

button div {
  display: block;
  width: 100%;
  height: 5px;
  margin: 6px 0px;
  background: gray;

  content: "";

  transition: 0.5s ease-in-out;
}

button.active {
  transform: rotate(-180deg);
}

.row-1.active {
  transform: rotate(25deg) translate(2px, 2px);
  border-radius: 33%;
}

.row-2.active {
  opacity: 0;
}

.row-3.active {
  transform: rotate(-25deg) translate(2px, -2px);
  border-radius: 33%;
}
</style>
