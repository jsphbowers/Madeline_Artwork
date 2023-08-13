<template>
  <div class="container-fluid">
    <section class="row justify-content-center">
      <div class="col-10">
        <h1 class="text-center">Portfolio</h1>
        <div class="masonry-with-columns">
          <img v-for="image in portfolio_images" :key="image" class="art-img" :src="image" />
        </div>
        <!-- <img class="art-img" src="src\assets\img\Art Work\Live Photos\Portfolio\Cat_Butterfly.jpeg" /> -->
      </div>
      <div class="col-10">
        <h1 class="text-center">Client Work</h1>
        <div class="masonry-with-columns">
          <img v-for="image in client_images" :key="image" class="art-img selectable" data-toggle="modal"
            data-target="#exampleModal" :src="image" />
        </div>
      </div>
    </section>

  </div>
</template>

<script>
export default {
  setup() {
    return {

      portfolio_images: ["src/assets/img/Art Work/Live Photos/Portfolio/Cat_Butterfly.jpeg", "/src/assets/img/Art Work/Live Photos/Portfolio/cougar.jpeg", "src/assets/img/Art Work/Live Photos/Portfolio/Face_W_Snake.jpeg", "/src/assets/img/Art Work/Live Photos/Portfolio/Skull_cocktail2.jpg", "src/assets/img/Art Work/Live Photos/Portfolio/Skull_Cropped.jpg", "/src/assets/img/Art Work/Live Photos/Portfolio/SnakeSkulls.jpg", "src/assets/img/Art Work/Live Photos/Portfolio/Wolf_half.jpg"],

      client_images: ["src/assets/img/Art Work/Live Photos/Client Work/Geometric.png", "src/assets/img/Art Work/Live Photos/Client Work/Half_Face_Letterboxed.png", "src/assets/img/Art Work/Live Photos/Client Work/Horse_W_Tree.png", "src/assets/img/Art Work/Live Photos/Client Work/Lion_LetterBoxed.png", "src/assets/img/Art Work/Live Photos/Client Work/Native_American_Letterboxed.png", "src/assets/img/Art Work/Live Photos/Client Work/Woman_by_Lake.jpeg"]
    }
  }
}
</script>

<style scoped lang="scss">
.masonry-with-columns {
  columns: 3 200px;
  column-gap: 2rem;
  padding-left: 3em;
  padding-right: 3em;
  padding-top: 1em;

  .art-img {
    width: 150px;
    color: white;
    margin: 0 1rem 1rem 0;
    display: inline-block;
    width: 100%;
    text-align: center;
    font-family: system-ui;
    font-weight: 900;
    font-size: 2rem;
    border-radius: 8px;
  }
}
</style>
