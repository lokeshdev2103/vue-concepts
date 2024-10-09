<template>
    <div>
      <button @click="toggleVisibility">Toggle Message</button>
      <p v-show="isVisible">This message is conditionally visible!</p>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const isVisible = ref(true);
  
      function toggleVisibility() {
        isVisible.value = !isVisible.value;
      }
  
      return { isVisible, toggleVisibility };
    },
  };
  </script>
 
  