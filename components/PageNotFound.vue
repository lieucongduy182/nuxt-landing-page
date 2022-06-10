<template>
  <div class="container">
    <h1>Page Not Found</h1>
    <img :src="require(`~/assets/images/fe25.jpg`)" alt="not-found">
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 5rem;
}
img {
  width: 15rem;
  margin: 0 auto;
}
</style>
