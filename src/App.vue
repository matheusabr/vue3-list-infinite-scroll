<template>
  <div class="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: {
    Header,
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
</style>
