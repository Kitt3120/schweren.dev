<template>
  <div class="home">
    <h1>This is the home page</h1>
    <p>Counter: {{ counter }}</p>
    <button @click="counter++">Increment</button>
  </div>
</template>

<style scoped></style>

<script setup lang="ts">
import { Ref, ref } from "vue";

const counter: Ref<number> = ref(0);
</script>
