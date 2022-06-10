<template>
  <div>
    <b-button id="show-btn" @click="showModal">
      Rent
    </b-button>

    <b-modal ref="my-modal" hide-footer title="Rent Modal">
      <div class="calendar-container">
        <div class="text-container">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit
            tenetur hic aperiam, architecto excepturi corrupti fugiat at eum
            quos perferendis reiciendis porro ratione aliquid perspiciatis,
            molestias blanditiis nulla deleniti temporibus.
          </p>
        </div>
        <vc-date-picker :value="null" color="indigo" is-dark is-range />
      </div>
      <b-button
        id="show-btn"
        variant="outline-danger"
        @click="addItem(product.id), hideModal()"
      >
        Order
      </b-button>
    </b-modal>
  </div>
</template>

<script>
export default {
  props: ['product'],
  methods: {
    showModal () {
      this.$refs['my-modal'].show()
    },
    hideModal () {
      this.$refs['my-modal'].hide()
    },
    addItem (id) {
      this.$store.dispatch('addItem', id)
    }
  }
}
</script>
<style scoped>
button {
  width: 100%;
  border: none;
  color: white;
  font-weight: 700;
  padding: 1rem 4rem;
  background-color: rgb(231, 81, 43);
  border-radius: 100rem;
  transition: 0.75s;
}
.calendar-container {
  margin: 0 auto;
  justify-content: space-between;
  display: flex;
  padding-bottom: 1.5rem;
}
.text-container {
  padding: 0.5rem;
}
</style>
