<template>
  <List
    @on-item-selected="onMovieSelected"
    :dataList="movieList"
    :selectedId="selectedId"
  />
</template>

<script>
import List from "./List.vue";

export default {
  name: "MovieList",
  components: {
    List,
  },
  props: {
    movieList: Array,
    selectedId: String,
  },
  methods: {
    onMovieSelected(movieData) {
      console.log(movieData);
      this.$emit("movie-selected", movieData);
    },
  },
};
</script>
