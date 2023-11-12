<template>
  <v-app>
    <TopNav></TopNav>
    <router-view></router-view>
    <Hero></Hero>

  </v-app>
</template>


<script>
import TopNav from './components/TopNav.vue'
import Hero from './components/Hero.vue'


export default {
  name: 'App',

  components: {
    TopNav,
    Hero
  },

  data: () => ({
    //
  }),
}
</script>
<style>
</style>
