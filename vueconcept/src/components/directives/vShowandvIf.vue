<template>
  <div>
    <button @click="toggle">Toggle Visibility</button>
    <p v-show="isVisible">This is toggled by v-show</p>
    
  <div>
    <p v-if="isVisible">Visible Content</p>
    <p v-else>Not Visible</p>
  </div>
  </div>
</template>

<script setup lang="ts">
  import { ref } from "vue";
      const isVisible = ref(true);
      const toggle = () => {
        isVisible.value = !isVisible.value;
      };
</script>

<!--
Difference Between v-if and v-show 

v-if : 
Element is added/removed from the DOM.
it completely true or false .

v-show : 
Element is always in the DOM.
it may be true or false 
-->