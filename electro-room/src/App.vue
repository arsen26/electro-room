<template>
  <v-app>
    <v-row>
      <v-col>
        <TopNav/>
      </v-col>
      <v-col>
        <NavBar/>
      </v-col>
    </v-row>
  </v-app>
</template>


<script>
import TopNav from './components/TopNav.vue'
import NavBar from './components/NavBar.vue'


export default {
  name: 'App',

  components: {
    TopNav,
    NavBar
  },

  data: () => ({
    //
  }),
}
</script>
<style>
</style>
