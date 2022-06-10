<template>
  <div>
    <h3>Customers Review</h3>
    <div v-if="!$fetchState.pending">
      <ReviewCard
        v-for="review in reviews"
        :key="review.login.uuid"
        :review="review"
      />
    </div>
    <div v-else>
      Loading ...
    </div>
  </div>
</template>

<script>
/* eslint-disable no-console */
export default {
  data () {
    return {
      reviews: []
    }
  },
  async fetch () {
    try {
      const response = await this.$axios.$get(
        'https://randomuser.me/api/?results=5'
      )
      this.reviews = response.results
    } catch (error) {
      console.log(error.massage)
    }
  }
}
</script>

<style></style>
