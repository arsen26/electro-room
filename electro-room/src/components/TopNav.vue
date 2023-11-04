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
      ]
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

.title {
  margin-top: 5px; /* Ndrysho vlerën sipas preferencës suaj */
  color: white;
}
.col-style{
  padding: 10px;
  padding-left: 10px;
}

</style>