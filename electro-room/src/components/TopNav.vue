<template>
  <v-app>
    <v-main>
  <nav class="navigation-bar d-none my--1 d-md-block">
    <v-container class="top-nav">
      <v-row>
        <v-col class="col-style" cols="18" v-for="(topheader, i) in topHeaders" :key="i">
          <div class="top-text">
            <svg-icon class="icons" type="mdi" :path="topheader.path"></svg-icon>
            <a href="">
              <span class="title">{{ topheader.title }}</span>
            </a>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <!-- ********************** NAV BAR **************************************-->
    <v-toolbar class="navbar">
        <span class="hidden-sm-and-up">
          <v-toolbar-side-icon @click="sidebar = !sidebar">
          </v-toolbar-side-icon>
        </span>
        <v-toolbar-title>
          <v-img class="img" src="electrRoomHorizontal-removebg.png">            
          </v-img>
        </v-toolbar-title>
        <v-autocomplete
        class="search-nav"
  clearable
  label="Kerko per produkt"
  :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
  variant="underlined"
></v-autocomplete>

        
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-xs-only nav-font">
          <v-btn
            
            v-for="item in menuItems"
            :key="item.title"
            :to="item.path">
            {{ item.title }}
          </v-btn>
          <v-btn class="sign">
            Sign IN/OUT
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>

  </nav>
</v-main>
  </v-app>
</template>
<script>
import SvgIcon from '@jamescoyle/vue-icon'
import * as mdijs from '@mdi/js'

export default{
  components: {
    SvgIcon,
  },

  data (){
    return{
      topHeaders:[
        {
          title:"Sherbimi i klientit",
          path: mdijs.mdiMenuDown,
        },
        {
          title:"Blog",
          path: mdijs.mdiMenuDown
        },
        {
          title:"Ide Dhuratash",
          path:mdijs.mdiMenuDown
        },
        {
          title:"Puno me ne",
          path: mdijs.mdiMenuDown
        }
      ],
      appTitle: 'Awesome App',
        sidebar: false,
        menuItems: [
            { title: 'Home', path: '/home', icon: 'home' },
            { title: 'Produktet', path: '/signup', icon: 'face' },
            { title: 'Lajmet e fundit', path: '/signin', icon: 'lock_open' }
       ],
       
    }
  }
}


</script>
<style>
.navigation-bar{
  display: flex;
  background-color: #071318;
  margin: -10px;
  margin-bottom: 40px;
  height: 32px;

}
.top-text {
  display: flex;
  align-items: center;
  color: white;
  padding-top: -30px;
  margin-top: -7px; 

}

.icons {
  height: 20px;
  width: 30px;
  color: rgb(255, 255, 255);
  margin-top: 3px;
  margin-right: -5px; 
}
.wider-autocomplete .v-input__slot {
  width: 300px; /* Shtoni gjerësinë që dëshironi */
}

.title {
  margin-top: 5px; /* Ndrysho vlerën sipas preferencës suaj */
  color: white;
}
.col-style{
  padding: 10px;
  padding-left: 10px;
}

.navbar{
  margin-top: -14px;
  padding-bottom: 10px;
  background-color: #0E2730;
}

.nav-font{
  color: white;
  padding: 10px;
  padding-right: 10px;
  font-size:larger;
}
.img{
  margin-top: 12px;
  margin-left: -30px;
  height: 220px;
}
.sign{
  padding-right: 50px;
}
.search-nav{
  color: white;
  margin-bottom: -30px;
  margin-right: -170px;
  width: 10px !important;
  height: min-content;
}
.centered-autocomplete {
  margin-top: -10px; /* Vendos tekstin në qendër vertikalisht */
  max-height: 50px; /* Përshtatni gjerësinë që dëshironi */
} 
</style>