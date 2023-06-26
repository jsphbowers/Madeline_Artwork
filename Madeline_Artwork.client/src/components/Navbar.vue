<template>
  <div class="container-fluid">
    <section class="row justify-content-center">
      <div class="col-10 d-flex flex-column align-items-center">
        <img src="../assets/img/temp-logo.png" alt="a line drawing of mushrooms" class="hero-img">
        <h1 class="cursive">New Earth Designs</h1>
      </div>
      <div class="col-10">
        <!-- insert new nav component here -->
      </div>
    </section>
  </div>
</template>

<script>
export default {
  setup() {
    return {}
  }
}
</script>
<style scoped lang="scss">
.hero-img {
  object-fit: cover;
  object-position: center;
  height: 40vh;
}

.cursive {
  font-family: 'Allura', cursive;
}
</style>
