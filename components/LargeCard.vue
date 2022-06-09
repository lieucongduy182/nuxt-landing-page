<template>
  <div class="card">
    <img
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt="card-item"
      class="image"
    >
    <h5 class="header">
      {{ card.title }}
    </h5>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      default: Object
    }
  }
}
</script>

<style scoped>
.card {
  width: 31.5%;
  min-height: 20rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  margin-top: 0.4rem;
}
.header:hover {
  text-decoration: underline;
}
.snippet {
  color: gray;
}
</style>
