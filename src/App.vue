<template>
  <div id="app">
    <div v-html="sampleMd"></div>
  </div>
</template>

<script>
import sampleMd from "@/assets/markdowns/sample.md";

export default {
  created() {
    this.sampleMd = sampleMd;
  }
};
</script>
