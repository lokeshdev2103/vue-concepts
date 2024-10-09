<template>
  <div>
    <button @click="awesome = !awesome">Toggle</button>
    <h1 v-if="awesome">Vue is awesome!</h1>
    <h1 v-else>Oh no 😢</h1>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const awesome = ref<boolean>(false);
</script>
