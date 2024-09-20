<template>
    <div :class="{ active: isActive, 'text-danger': hasError }" 
         :style="{ color: textColor, fontSize: fontSize + 'px' }">
      This div has both dynamic classes and styles.
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const isActive = ref(true);
      const hasError = ref(false);
      const textColor = ref('purple');
      const fontSize = ref(30);
  
      return {
        isActive,
        hasError,
        textColor,
        fontSize,
      };
    },
  };
  </script>
  
  <style>
  .active {
    color: green;
  }
  .text-danger {
    color: red;
  }
  </style>
  