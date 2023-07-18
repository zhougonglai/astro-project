<template>
  <div class="counter">


    <lottie-player src="https://lottie.host/a2e2672b-8eb4-4d29-9178-fef08113be40/7J4uNyRxoh.json" background="transparent"
      style="width: 300px; height: 300px;" loop count="2" hover autoplay></lottie-player>
  </div>
  <div class="counter-message">
    <slot />
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const count = ref(0);
const add = () => (count.value = count.value + 1);
const subtract = () => (count.value = count.value - 1);
</script>

<style>
.counter-message {
  text-align: center;
}
</style>
