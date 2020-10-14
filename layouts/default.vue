<template>
  <v-app>
    <v-content class="default-layout">
      <v-container class="default-layout__container">
        <div class="default-layout__container__header">
          <h2>Нурсеит Шарип</h2>
          <NavbarComponent />
        </div>
        <div class="default-layout__container__content">
          <nuxt/>
        </div>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from "@/components/Navbar/index"
export default {
  components: {
    NavbarComponent: Navbar
  },
  data() {
    return {}
  }
}
</script>

<style lang="scss">
.default-layout {
  &__container {
    max-width: 900px;
    &__header {
      margin-bottom: 25px;
    }
  }
}
</style>
