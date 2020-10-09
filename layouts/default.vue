<template>
  <v-app>
    <v-content class="default-layout">
      <v-container class="default-layout__container">
        <div>
          <NavbarComponent />
        </div>
        <div>
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
  }
}
</style>
