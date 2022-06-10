<template>
  <div class="review-card">
    <div class="image-card">
      <img :src="review.picture.medium" alt="image-user">
    </div>
    <div class="text-card">
      <h6>{{ review.name.first + ' ' + review.name.last }}</h6>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed, voluptas
        fugiat saepe ratione commodi illo, alias corporis cum ipsam quas magni
        explicabo eveniet, error ea libero amet dolores tempore nobis.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['review']
}
</script>

<style>
.review-card {
  margin-top: 1.5rem;
  height: 5rem;
  display: flex;
}
.image-card {
  width: 4rem;
  height: 4rem;
  border-radius: 100%;
}
.text-card {
  margin-left: 2rem;
}
p {
  color: gray;
}
</style>
