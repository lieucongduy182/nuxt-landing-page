<template>
  <div class="container">
    <img
      :src="require(`~/assets/images/${myRent.image}`)"
      alt="item"
      class="image"
    >

    <div class="text-container">
      <h5>{{ myRent.title }}</h5>
      <p>{{ myRent.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['myRent']
}
</script>

<style scoped>
.container {
  display: flex;
  margin: 3rem auto;
}
.image {
  width: 17.5rem;
  height: 15rem;
  border-radius: 0.5rem;
}
.text-container {
  padding: 0 1rem;
}
p {
  color: grey;
}
</style>
