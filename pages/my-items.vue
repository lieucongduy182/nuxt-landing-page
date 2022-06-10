<template>
  <div class="container py-5">
    <nuxt-link to="/">
      Go back
    </nuxt-link>
    <MyItem v-for="myRent in myRentals" :key="myRent.id" :myRent="myRent" />
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: {
    ...mapState(['myRentals'])
  }
}
</script>

<style scoped></style>
