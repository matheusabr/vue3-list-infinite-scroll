<template>
  <div class="movie-list">
    <div class="list-item">
      <div class="rank-container">
        <div class="rank-content">
          <h5>Rank</h5>

          <h1>3</h1>
        </div>
      </div>

      <div class="item-content">
        <div class="item-header">
          <h2>Split</h2>

          <span class="year">(2016)</span>
        </div>

        <div class="item-footer">
          <span class="revenue">Revenue</span>

          <h4>$138.12</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MovieList',
};
</script>

<style scoped>
.list-item {
  display: flex;
  padding: 20px 10px;
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

.item-header {
  display: flex;
}

.item-header > .year {
  padding-left: 10px;
  font-size: 10px;
}

.item-footer > .revenue {
  font-size: 10px;
}
</style>
