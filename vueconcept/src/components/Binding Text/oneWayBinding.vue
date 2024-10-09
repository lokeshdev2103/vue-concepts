<template>
    <div>
        <h1>{{ textInterpolation }}</h1>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const textInterpolation = ref<string>("one way binding");
</script>


<!-- 
one way Binding :
Data flows from the Vue instance to the template
-->
