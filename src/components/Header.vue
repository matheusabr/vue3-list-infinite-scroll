<template>
  <div class="header">
    <h1>MoviesDB</h1>

    <span>FILTER</span>
  </div>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped>
.header {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100px;
  padding: 20px 10px;
  background-color: #dedede;
}
</style>
