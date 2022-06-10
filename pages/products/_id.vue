<template>
  <div v-if="product" class="container py-5">
    <div class="hero-container">
      <img
        :src="require(`@/assets/images/${product.image}`)"
        alt="image"
        class="image"
      >
      <div class="info-box">
        <h2>{{ product.title }}</h2>
        <p class="snippet">
          {{ product.snippet }}
        </p>
        <RentModal :product="product" />
      </div>
    </div>
    <div class="whats-included-container">
      <div class="included-container">
        <h6>Supper Effective</h6>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam
          excepturi commodi natus dolorem, earum, cupiditate facilis tempore
          aspernatur eius ullam distinctio ducimus assumenda rerum reiciendis
          molestias dolore ratione suscipit beatae.
        </p>
      </div>
      <div class="included-container">
        <h6>Clean & Tidy</h6>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis
          similique omnis, delectus ratione explicabo natus ad sit a, beatae hic
          exercitationem. Quaerat, et praesentium neque placeat exercitationem
          veniam ratione repellat.
        </p>
      </div>
      <div class="included-container">
        <h6>Cancel Anytime</h6>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem ratione
          explicabo corporis at, aspernatur est nisi quisquam dolorem quis
          voluptatibus ipsa veritatis asperiores dignissimos animi reiciendis
          cupiditate placeat quaerat sint?
        </p>
      </div>
      <div class="included-container">
        <h6>Satisfaction Guaranteed</h6>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi
          mollitia veniam cupiditate aliquid, qui illum, iste facilis debitis
          eius quasi vero! Recusandae a quia incidunt id, consequuntur quaerat
          nulla fuga.
        </p>
      </div>
    </div>
    <div class="description-container">
      <p>
        {{ product.description }}
      </p>
    </div>
    <Reviews />
  </div>
  <div v-else class="container padding">
    <PageNotFound />
  </div>
</template>

<script>
export default {
  computed: {
    product () {
      return this.$store.getters.getProductById(this.$route.params.id)
    }
  }
}
</script>

<style scoped>
.hero-container {
  display: flex;
  justify-content: space-between;
}
.image {
  width: 59%;
  height: 25rem;
}
.info-box {
  width: 41%;
  background-color: rgba(207, 207, 201, 0.322);
  padding: 1rem;
  border-radius: 0.5rem;
  margin-left: 1.5rem;
}
.snippet {
  color: gray;
}
.whats-included-container {
  border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
}
.included-container {
  margin-top: 1.5rem;
}
.description-container {
  border-bottom: 0.1rem solid rgba(182, 128, 128, 0.151);
  margin: 3rem 0;
  color: gray;
}
</style>
