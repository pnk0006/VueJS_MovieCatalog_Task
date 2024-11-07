<template>
  <img class="poster" :src="posterUrl" :alt="movieTitle" />
</template>

<script>
export default {
  name: "Poster",
  props: {
    movieTitle: String,
    posterUrl: String,
  },
};
</script>

<style scoped>
.poster {
  border-radius: 5%;
  max-width: 48vh;
  max-height: 60vh;
  width: auto;
  height: auto;
}
</style>