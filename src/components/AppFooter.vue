<script>
'./assets/img/footer-bg.jpg'
export default {
  data() {
    return {
      imgBg: "footer-bg"
    };
  },
  methods: {
    getImageUrl(imageName) {
      return new URL(`./img/${imageName}.jpg`, import.meta.url).href;
    },
  },
};
</script>

<template>
<footer class="container">
  <div class="footer-text">
    <div class="list">
    <h2>DC COMICS</h2>
    <ul>
      <li>Characters</li>
      <li>Comics</li>
      <li>Movies</li>
      <li>Tv</li>
      <li>Games</li>
      <li>Videos</li>
      <li>News</li>
    </ul>
    <br>
    <h2>SHOP</h2>
    <ul>
      <li>Characters</li>
      <li>Comics</li>
    </ul>
    </div>

    <div class="list">
    <h2>DC</h2>
    <ul>
      <li>Characters</li>
      <li>Comics</li>
      <li>Movies</li>
      <li>Tv</li>
      <li>Games</li>
      <li>Videos</li>
      <li>News</li>
      <li>Characters</li>
      <li>Comics</li>
    </ul>
    </div>

    <div class="list">
    <h2>SITES</h2>
    <ul>
      <li>Characters</li>
      <li>Comics</li>
      <li>Movies</li>
      <li>Tv</li>
      <li>Games</li>
    </ul>
    </div>
  </div>
  <div class="footer-social">

  </div>
</footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.footer-text {
  @include flex(row, Start, start);
};

.container {
    background-image: url("./img/footer-bg.jpg")
}

.footer-text {
  color: white;
  max-width: 70%;
    margin: 0 auto;
    padding: 20px;
}

.list {
  padding:  20px;
}
</style>