<!-- 
what is ref in compositonal api 


The way to create reactive reference to value 
You can access the value of a ref using the .value property
it is applicable for primitive data types only .


-->

<template>
    <div>{{ abc }}</div>
</template>
<script setup lang="ts">
import { ref } from 'vue';

const abc = ref('loki');
console.log(abc.value);
</script>

