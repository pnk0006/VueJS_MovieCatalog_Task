<template>
  <div class="movieCatalogueWrapperStyle">
    <div class="moviePreviewWrapperStyle">
      <MoviePreview
        :movieTitle="selectedMovie.title"
        :posterUrl="selectedMovie.poster"
        :releaseYear="selectedMovie.year"
        :director="selectedMovie.director"
        :casts="selectedMovie.casts"
        :genre="selectedMovie.genre"
      />
    </div>
    <div class="movieListWrapperStyle">
      <MovieList
        :movieList="movieList"
        :selectedId="selectedMovie.id"
        @movie-selected="onMovieSelected"
      />
    </div>
  </div>
</template>

<script>
import MovieList from "@/components/molecule/MovieList.vue";
import MoviePreview from "@/components/molecule/MoviePreview.vue";

export default {
  name: "MovieCatalogue",
  components: {
    MovieList,
    MoviePreview,
  },
  props: {
    movieList: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
  data() {
    return {
      selectedMovie: this.movieList.length ? this.movieList[0] : {},
    };
  },
  methods: {
    onMovieSelected(movieData) {
      this.selectedMovie = movieData;
      this.$emit("movie-selected", movieData);
    },
  },
};
</script>

<style scoped>
.movieCatalogueWrapperStyle {
  height: 100%;
  overflow: hidden;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  width: 100%;
}

.moviePreviewWrapperStyle,
.movieListWrapperStyle {
  flex: 1 1 50%;
  height: calc(100vh - 60px);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.moviePreviewWrapperStyle {
  text-align: center;
  margin-right: 1em;
  align-self: flex-start;
}

.movieListWrapperStyle {
  text-align: left;
  align-self: flex-end;
}
</style>
