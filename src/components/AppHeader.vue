<script>
export default {
  data() {
    return {
      menu: [
        {
          title: "Characters",
          isActive: false,
        },
        {
          title: "Comics",
          isActive: false,
        },
        {
          title: "Movies",
          isActive: false,
        },
        {
          title: "Tv",
          isActive: false,
        },
        {
          title: "Games",
          isActive: true,
        },
        {
          title: "Collectibles",
          isActive: false,
        },
        {
          title: "Videos",
          isActive: false,
        },
        {
          title: "Fans",
          isActive: false,
        },
        {
          title: "News",
          isActive: false,
        },
        {
          title: "Shop",
          isActive: false,
        },
      ],
    };
  },
};
</script>

<template>
    <header class="header-dc">
    <div class="header-logo">
      <img
        src="/img/dc-logo.png"
        alt="Logo della Dc"
      />
    </div>
    <ul class="navigation">
      <li v-for="item in menu">
        <a href="" :class="{ active: item.isActive }">{{ item.title }}</a>
      </li>
    </ul>
    </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

  .header-logo {
    text-align: center;
  }

  .navigation {
    @include flex(row, space-between, center);
  }

  .header-dc {
    @include flex(row, space-between, center);
    max-width: 70%;
    margin: 0 auto;
    padding: 20px;
  }

  ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: 1rem;
    margin-top: 26px;

    ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: 1rem;
    margin-top: 26px;

    a {
      padding: 10px 16px;
      text-decoration: none;
      color: $text-color;
      display: inline-block;
        
      &:hover {
        color: $primary-dark;
      }

      &.active {
        background-color: $primary-color;
      }
    }
  }
}
</style>