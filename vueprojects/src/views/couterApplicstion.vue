<template>
  <div>
    <h1>Couter Application</h1>
    <button class="spacing" @click="increment">+</button>
    <span class="spacing">{{ count }}</span>
    <button class="spacing" @click="decrement">-</button>
    <p v-if="errorMessage">{{ errorMessage }}</p>
  </div>
</template>
<script lang="ts">
import { ref, watch } from "vue";

export default {
  setup() {
    const count = ref<number>(0);
    const errorMessage = ref<string>();
    const increment = () => {
      if (count.value <= 14) {
        errorMessage.value = "";
        count.value++;
      } else {
        errorMessage.value = "not more than 15 number";
      }
    };

    const decrement = () => {
      if (count.value >= 0) {
        count.value--;
        errorMessage.value = "";
      } else {
        errorMessage.value = "number should not be negative";
      }
    };

    return {
      count,
      increment,
      decrement,
      errorMessage,
    };
  },
};
</script>

<style scoped>
.spacing {
  margin: 10px;
}
</style>
