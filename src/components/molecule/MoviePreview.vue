<template>
  <div class="movie-previe-container">
    <Poster :movieTitle="movieTitle" :posterUrl="posterUrl" />
    <MovieLabel :title="movieTitle" :year="releaseYear" />
    <MovieInfo label="Director" :value="director" />
    <MovieInfo label="Cast" :value="casts" />
    <MovieInfo label="Genre" :value="genre" />
  </div>
</template>

<script>
import Poster from "../atom/Poster.vue";
import MovieLabel from "../atom/MovieLabel.vue";
import MovieInfo from "../atom/MovieInfo.vue";

export default {
  name: "MoviePreview",
  props: {
    movieTitle: String,
    posterUrl: String,
    releaseYear: String,
    director: String,
    casts: String,
    genre: String,
  },
  components: {
    Poster,
    MovieLabel,
    MovieInfo,
  },
};
</script>

<style scoped>
.movie-previe-container {
  padding-top: 10px;
}
</style>
