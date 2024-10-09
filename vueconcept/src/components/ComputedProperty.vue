<!-- 

it is also one of the way to display the data in UI

computed property is a reactive property that is derived from other reactive data.

define a value that automatically recalculates when its dependencies change 

-->

<template>
    <div>
      <input v-model="firstName" placeholder="First Name" />
      <input v-model="lastName" placeholder="Last Name" />
      <p>Full Name: {{ fullName }}</p>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, computed } from 'vue';

      const firstName = ref('');
      const lastName = ref('');
  
      const fullName = computed(() => {
        return `${firstName.value} ${lastName.value}`.trim();
      });
  </script>