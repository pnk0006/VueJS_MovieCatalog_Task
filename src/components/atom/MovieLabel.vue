<template>
  <h3>{{ title }} ({{ year }})</h3>
</template>

<script>
export default {
  name: "MovieLabel",
  props: {
    title: String,
    year: String,
  },
};
</script>

<style scoped>
</style>