<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark p-3">
    <nuxt-link class="navbar-brand" to="/">
      Firegngii
    </nuxt-link>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon" />
    </button>

    <div id="navbarSupportedContent" class="collapse navbar-collapse">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item active">
          <nuxt-link
            class="nav-link"
            to="/products"
          >
            Products <span class="sr-only">(current)</span>
          </nuxt-link>
        </li>
        <li class="nav-item active">
          <nuxt-link
            class="nav-link"
            to="/my-items"
          >
            My Items <span class="sr-only">(current)</span>
          </nuxt-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped></style>
