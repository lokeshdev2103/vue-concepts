<template>
    <div>
        <h1>{{ textInterpolation }}</h1>
        <div>
            <input v-model="twowaybinding" type="text" placeholder="enter the name" />
        </div>
        <p>{{ twowaybinding }}</p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const textInterpolation = ref<string>("one way binding");
const twowaybinding  = ref<string>('')
</script>


<!-- 
one way Binding :
Data flows from the Vue instance to the template

two way binding : 
Data flows from the vue instance to the template and template to vue script.

-->
