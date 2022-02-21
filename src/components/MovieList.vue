<template>
  <h3 class="loading" v-if="loading">Loading...</h3>

  <div class="movie-list">
    <div v-for="movie in movieList" class="list-item">
      <div class="rank-container">
        <div class="rank-content">
          <h5>Rank</h5>

          <h1>{{ movie.rank }}</h1>
        </div>
      </div>

      <div class="item-content">
        <div class="item-info">
          <h2>{{ movie.title }}</h2>

          <span v-if="movie.year" class="year">({{ movie.year }})</span>
        </div>

        <div v-if="movie.revenue" class="item-extra">
          <span class="revenue">Revenue</span>

          <h4>${{ movie.revenue }}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const API_URL = 'https://movie-challenge-api-xpand.azurewebsites.net/api';

export default {
  name: 'MovieList',

  data: () => ({
    loading: true,
    movieList: [],
  }),

  created() {
    // Request api data on init
    this.fetchData();
  },

  methods: {
    async fetchData() {
      const url = `${API_URL}/movies`;
      const data = await (await fetch(url)).json();
      this.movieList = data.content;
      this.loading = false;
    },
  },
};
</script>

<style scoped>
.list-item {
  display: flex;
  padding: 20px 10px 0 10px;
}

.rank-container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 80px;
  height: 60px;
  background-color: #cdcdcd;
}

.rank-container > .rank-content {
  text-align: center;
}

.item-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 10px;
  background-color: #efefef;
}

.item-info {
  display: flex;
}

.item-info > .year {
  padding-left: 10px;
  font-size: 10px;
}

.item-extra {
  padding-left: 10px;
}

.item-extra > .revenue {
  font-size: 10px;
}
</style>
