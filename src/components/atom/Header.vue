<template>
  <div class="header-container">
    <h1>🎥 {{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "title-header",
  props: {
    title: String,
  },
};
</script>

<style scoped>
.header-container {
  min-height: 60px;
  background-color: rgb(32, 35, 42);
  color: rgb(255, 255, 255);
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
</style>
