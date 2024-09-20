<template>

<div>
    <input v-model="inputValue" />
    <p>{{ inputValue }}</p>
</div>

</template>
  
<script lang="ts">
import { ref } from "vue";

const inputValue = ref<string>("");
</script>
  