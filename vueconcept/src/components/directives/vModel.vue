<template>
  <div>
    <input v-model="inputValue" type="text" />
    <div>
      <p>{{ inputValue }}</p>
    </div>
  </div>
</template>
  
<script setup lang="ts">
import { ref } from "vue";
const inputValue = ref<string>('');
</script>
