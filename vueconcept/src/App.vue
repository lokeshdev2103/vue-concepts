<script lang="ts">
import textBinding from "./components/Bindings/dataBinding.vue";
import classandstyleBinding from "./components/Bindings/classandstyleBinding.vue";
import vModel from "./components/directives/vModel.vue";

export default {
  components: {
    textBinding,
    classandstyleBinding,
    vModel,
  },
  setup() {
    return {};
  },
};
</script>

<template>
  <div>
    <textBinding />
    <classandstyleBinding />
    <vModel />
  </div>
</template>

