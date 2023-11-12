    <template>
    <v-row class="row-hero">
     <v-col class="col-category" cols="2">
        <div  v-for="(item, i) in categoryTitle" class="categories-title-style">
            <svg-icon class="category-icon" type="mdi" :path="item.path"></svg-icon>

            {{item.title}}
        </div>
  <v-row v-for="(category, i) in categories" :key="i">

    <v-btn class="button-style" variant="text">
        <svg-icon class="button-icon" type="mdi" :path="category.path"></svg-icon>

        {{ category.title }}
</v-btn>
  </v-row>
</v-col>
    <v-col>
        <v-card
    class="card-hero-style"
    max-width="450"
  >
  <v-img
   class="card-hero-image"
   :src="require('@/assets/headset.png')"
   cover
></v-img>

  </v-card>
    </v-col>
    </v-row>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon'
import * as mdijs from '@mdi/js'



    export default {
        components: {
    SvgIcon,
  },


        data (){
            return{
                categoryTitle:[
                    {
                        title:'All Categories',
                        path: mdijs.mdiMenu
                    }
                ],

                categories:[
                    {
                        title:"Mouse",
                        path:  mdijs.mdiMouse
                    },
                    {
                        title:"Tastier",
                        path:  mdijs.mdiKeyboard
                        
                    },
                    {
                        title:"Desktop",
                        path:  mdijs.mdiDesktopTower
                    },
                    {
                        title:"Fisha",
                        path:  mdijs.mdiCableData
                    },
                    {
                        title:"Kufje",
                        path:  mdijs.mdiHeadset
                    },
                    {
                        title:'Printer',
                        path:  mdijs.mdiPrinterOutline
                    },
                    {
                        title:'Laptop',
                        path:  mdijs.mdiLaptop
                    },
                    {
                        title:"Ekrane",
                        path:  mdijs.mdiMonitor
                    },
                    {
                        title:"Tablet",
                        path:  mdijs.mdiTablet
                    },
                    {
                        title:"Zyre",
                        path:  mdijs.mdiChairRolling
                    },
                    {
                        title:"Kontroller",
                        path:  mdijs.mdiController
                    }
                ]
            }
        }
    }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Big+Shoulders+Text:wght@100&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Gugi&display=swap');

.row-hero{
    margin-top: -950px;
    background-color: #194554;
}
.col-category{
    background-color: rgb(255, 255, 255);
    margin-top: 20px;
    margin-left: 20px;
    border-radius: 5px;
    height: 450px;
    width: 240px;
    font-family: 'Poppins';
    font-style: oblique 20deg;
}
.categories-style{
    
    font-family: 'Poppins';
    }
      
.categories-title-style{
    width: 240px;

    background-color: #5E7C87;
    color: white;
    border-radius: 10px;
    margin-top: -14px;
    margin-bottom: 20px;
    text-align: center;
    font-size: 25px;
    margin-left: -13px;
}
.category-icon{
    color: rgb(255, 255, 255);
    height: 30px;
    width: 40px;
    margin-left: -40px;
    margin-bottom: -8px;
}
.button-style{
    height: 30px !important;
}
.button-icon{
    color: black;
}
.card-hero-style{
    margin-top: 7px;
    margin-left: 10px;
    height: 450px;
}

.card-hero-image{
    width: 100% !important; 
    height: 100% !important; 
    object-fit: contain !important;
}
</style>

