<template>
  <div>
    <span>
      <strong>{{ label }}: </strong>
    </span>
    <span>{{ value }}</span>
  </div>
</template>

<script>
export default {
  name: "MovieInfo",
  props: {
    label: String,
    value: String,
  },
};
</script>

<style scoped>
</style>