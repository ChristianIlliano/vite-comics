<script>
export default {
  data() {
    return {
        icons: [
        {
          title: "Digital Comics",
          img: "buy-comics-digital-comics.png",
        },
        {
            title: "Dc Merchandise",
          img: "buy-comics-merchandise.png",
        },
        {
            title: "Subscription",
          img: "buy-comics-subscriptions.png",
        },
        {
            title: "Comic Shop Locator",
          img: "buy-comics-shop-locator.png",
        },
        {
            title: "Dc Power Visa",
          img: "buy-dc-power-visa.svg",
        }
      ]
    }
  }
}

</script>

<template>
  <header>
    <div class="b-bg">
        <div class="content"><H2> -->Content goes here<-- </H2></div>
    </div>
    <div class="blue-bg">
        <div class="content">
            <ul class="navigation">
                <li v-for="item in icons" class="li-icon">
                <img :src="`./img/${item.img}`" alt="">
                <a href="" :class="{ active: item.isActive }">{{ item.title }}</a>
                </li>
            </ul>
        </div>
    </div>
</header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.b-bg {
    background-color: #1c1c1c;
    color: white;
    padding: 40px 0;
}

.li-icon {
  @include flex(row, center, center);
  a {
    color: white;
  }
}

.blue-bg {
    background-color: #0282f9;
    color: white;
    padding: 40px 0;
}

.content {

    max-width: 70%;
    margin: 0 auto;
    padding: 20px;
}

.navigation {
    @include flex(row, center, center);
    img {
      max-height: 150px;
    }

    gap: 40px; 
    font-size: 1.4rem;
}
</style>