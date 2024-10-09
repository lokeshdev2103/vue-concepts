<template>
    <div>
        <div>
            <input v-model="twowaybinding" type="text" placeholder="enter the name" />
        </div>
        <p>{{ twowaybinding }}</p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const twowaybinding  = ref<string>('')
</script>


<!-- 
two way binding : 
Data flows from the vue instance to the template and template to vue script.
-->
