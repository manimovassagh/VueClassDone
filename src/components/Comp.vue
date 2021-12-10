<template>
  <div>
    <h1>This is composition {{ someText }}</h1>
    <div>{{ family }}</div>
  </div>
</template>

<script lang="ts">
import { ref } from "@vue/composition-api";

export default {
  setup() {
    const someText = ref("Sahar Composition");
    const family = ref("Morattab Composition");

    return { someText };
  },
};
</script>

<style></style>
