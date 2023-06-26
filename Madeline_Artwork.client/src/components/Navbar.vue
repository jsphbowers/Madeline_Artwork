<template>
  <div class="container-fluid">
    <section class="row justify-content-center">
      <div class="col-10 d-flex flex-column align-items-center">
        <img src="../assets/img/temp-logo.png" alt="a line drawing of mushrooms" class="hero-img">
        <h1 class="cursive">New Earth Designs</h1>
      </div>
      <div class="col-7 d-flex justify-content-between my-3">
        <router-link :to="{ name: 'Home' }" class="text-dark"
          :class="{ underline: route.name == 'Home' }">Home</router-link>
        <router-link :to="{ name: 'About' }" class="text-dark"
          :class="{ underline: route.name == 'About' }">About</router-link>
        <router-link :to="{ name: 'Shop' }" class="text-dark"
          :class="{ underline: route.name == 'Shop' }">Shop</router-link>
        <router-link :to="{ name: 'Contact' }" class="text-dark"
          :class="{ underline: route.name == 'Contact' }">Contact</router-link>
      </div>
    </section>
  </div>
</template>

<script>
import { useRoute } from "vue-router";
import { logger } from "../utils/Logger.js";
import { onMounted } from "vue"

export default {
  setup() {
    const route = useRoute()
    onMounted(() => logger.log(route))
    return {
      route,
    }
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

.underline {
  border-bottom: 2px solid olive
}
</style>
