<template>
  <v-app>
    <v-main>
      <Header />
      <Nuxt />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Header from "../components/global/Header.vue"
import Footer from "../components/global/Footer.vue"

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style>
* {
  overflow-x: hidden;
}
</style>
