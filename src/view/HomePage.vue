<template>
  <MovieCatalogue :movieList="movieData" @movie-selected="onMovieSelected" />
</template>

<script>
import MovieCatalogue from "../components/organism/MovieCatalogue";
import dataJson from "../static/movie-data.json";

export default {
  name: "HomePage",
  components: {
    MovieCatalogue,
  },
  data() {
    return {
      movieData: [],
    };
  },
  methods: {
    onMovieSelected(movie) {
      this.$emit("movie-selected", movie);
    },
  },
  created() {
    this.movieData = dataJson;
  },
};
</script>

<style scoped></style>
