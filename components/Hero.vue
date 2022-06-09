<template>
  <div class="Hero container">
    <div class="text-container">
      <h1 class="text-header">
        Find your Fire Extinguisher
      </h1>
      <p class="snippet">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint fugiat sit
        inventore amet. Et placeat assumenda iusto sequi corporis repellendus
        minima dignissimos in. Voluptatem quibusdam eaque praesentium
        exercitationem, recusandae delectus?
      </p>
      <button class="button btn">
        Start Looking
      </button>
    </div>
    <img class="image" src="~/assets/svg/fire-extinguisher.svg" alt="fire-extinguisher">
  </div>
</template>

<style scoped>
.Hero {
  min-height: 50vh;
  position: relative;
  display: flex;
  padding: 3rem 0;
  align-items: flex-start;
  justify-content: space-between;
}
.text-container {
  width: 50%;
  margin-top: 3rem;
}
.text-header {
  font-weight: 900;
  font-size: 4rem;
}
.snippet {
  color: grey;
  font-size: 1rem;
}
.image {
  width: 25.5rem;
  margin-top: 1.5rem;
}
.overlay {
  background: rgba(0, 0, 0, 0);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
.button {
  padding: 1rem 3rem;
  border-radius: 100rem;
  background-color: rgb(231, 81, 43);
  color: white;
  width: 20rem;
  font-weight: 700;
  transition: 0.5s;
}
.button:hover {
  width: 21.5rem;
}
@media (max-width: 500px) {
  .Hero {
    min-height: 40vh;
  }
}
</style>
