<template>
  <v-main class="navbar">
    <v-container class="navbar__items">
      <div class="navbar__items__name">
        <h3 class="text-h3">Нурсеит Шарип</h3>
      </div>
      <div class="navbar__items__menu">
        <v-tabs>
          <v-tab class="navbar__items__menu__item" v-for="(menu, index) in menus" :key="`menu-${index}`">
            <nuxt-link class="navbar__items__menu__link" :to="menu.link">{{ menu.name.ru }}</nuxt-link>
          </v-tab>
        </v-tabs>
      </div>
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
}
</script>

<style scoped lang="scss">
.navbar__items {
  &__name {
    margin-bottom: 15px;
  }
  &__menu {
    &__link {
      width: 100%;
      height: 100%;
    }
    &__item {
      padding: 0;
      width: max-content;
      min-width: 100px;
    }
  }
}
</style>
