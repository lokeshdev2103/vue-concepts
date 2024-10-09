<template>
  <div>
    <div v-for="name in names" :key="name.id">
      <h1>{{ name.fullName }}</h1>
      <h2>{{ name.age }}</h2>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref } from "vue";

const names = ref([{
    id: 23,
    fullName: "Pujitha",
    age: 26,
  },
  {
    id: 45,
    fullName: "Lokesh",
    age: 25,
  }
]);
</script>

<!--  
A directive in Vue.js that allows us to loop through an array or object and render a block of HTML for each item. It is commonly used to create lists or tables of data.

v-for="(item, index) in items"

item: The current item in the iteration.
index (optional): The index of the current item.
items: The array or object being iterated over.

for v-for :key required 

-->
