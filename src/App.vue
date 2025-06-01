<template>
  <v-app>
    <TopNav class="top-nav"></TopNav>
    <Hero></Hero>
    <productList></productList>
  </v-app>
</template>

<script>
import TopNav from './components/TopNav.vue'
import Hero from './components/Hero.vue'
import productList from './components/productList.vue'

export default {
  name: 'App',
  components: {
    TopNav,
    Hero,
    productList
  },
  data: () => ({
    //
  }),
}
</script>

<style scoped>

</style>
