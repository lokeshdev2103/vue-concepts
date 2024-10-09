<!--
what is reactive in compositional api 

The way to create reactive reference object or array .
You can access and modify properties directly without needing to use .value
it is applicable for non-primitive data types only 
-->


<template>
    <div>

    </div>
</template>
<script setup lang="ts">
import { reactive } from 'vue';

const state = reactive({
  count: 0,
  user: {
    name: 'Alice',
    age: 25,
  },
});

console.log(state.count);

</script>
