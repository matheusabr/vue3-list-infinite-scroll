<template>
  <div id="app">
    <Header />

    <MovieList />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import MovieList from './components/MovieList.vue';

export default {
  name: 'App',
  components: {
    Header,
    MovieList,
  },
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
  padding: 0;
}

h1,
h2,
h3,
h4,
h5 {
  margin: 0;
}

h1 {
  font-size: 24px;
}

h2 {
  font-size: 16px;
}

h3 {
  font-size: 14px;
}

h4 {
  font-size: 12px;
}

h5 {
  font-size: 10px;
}

.loading {
  padding: 20px;
  text-align: center;
}
</style>
