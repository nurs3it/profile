<template>
  <v-main class="navbar">
    <v-container class="navbar__items">
      <ul class="navbar__items__menu">
        <li class="navbar__items__menu__item subtitle-2"
            :class="{ 'active-route': menu.link === routeName }"
            v-for="(menu, index) in menus"
            @click="goto(menu.link)"
            :key="index"
        >
          {{ menu.name.ru }}
        </li>
      </ul>
    </v-container>
  </v-main>
</template>

<script>
import MenuList from "@/datas/menu.constant"

export default {
  name: "index",
  data() {
    return {
      menus: MenuList
    }
  },
  computed: {
    routeName() {
      return this.$route.path
    }
  },
  methods: {
    goto(link) {
      this.$router.push(link)
    }
  },
}
</script>

<style scoped lang="scss">
.navbar {
  .navbar__items {
    &__name {
      margin-bottom: 15px;
    }

    &__menu {
      &__link {
        width: 100%;
        height: 100%;
      }

      .active-route {
        border-bottom: 4px solid #ff7c00;
      }

      &__item {
        justify-content: center;
        cursor: pointer;
        align-items: center;
        width: max-content;
        min-width: 100px;
        padding: 10px;
        display: flex;
        float: left;
        transition: .1s ease-out;
        border-bottom: 2px solid transparent;

        &:hover {
          background: bisque;
          border-bottom: 4px solid #ff7c00;
        }
      }
    }
  }
}
</style>
