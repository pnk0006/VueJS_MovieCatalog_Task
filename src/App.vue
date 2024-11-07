<template>
  <div id="app">
    <Header :title="pageTitle" />
    <HomePage @movie-selected="updateSelectedMovieTitle" />
    <HomePage />
  </div>
</template>

<script>
import Header from "./components/atom/Header";
import HomePage from "./view/HomePage";

export default {
  name: "App",
  components: {
    Header,
    HomePage,
  },
  data() {
    return {
      pageTitle: "Kung Fu Panda",
    };
  },
  methods: {
    updateSelectedMovieTitle(movie) {
      this.pageTitle = movie.title;
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
