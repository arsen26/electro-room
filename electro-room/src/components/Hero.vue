        <template>
        <v-row class="row-hero">
        <v-col class="col-category" cols="2">
            <div  v-for="(item, i) in categoryTitle" :key="i" class="categories-title-style">
                <svg-icon class="category-icon" type="mdi" :path="item.path"></svg-icon>

                {{item.title}}
            </div>
            <!-- GJENERIMI I TE GJITHA KATEGORIVE-->
    <v-row v-for="(category, i) in categories" 
    :key="i">

        <v-btn class="button-style" variant="text">
            <svg-icon class="button-icon" type="mdi"  :path="category.path"></svg-icon>

            {{ category.title }}
    </v-btn>
    </v-row>
    </v-col>

    <!-- BANERI KRYESOR-->
        <v-col cols="3" >
            <v-card class="card-hero-style full-size">

    <v-img
    class="card-hero-image"
    :src="require('@/assets/headset.png')"
    cover
    
    ></v-img>
    </v-card>
        </v-col>
        
        <!-- GJENERIMI I KARTAVE QE DO JEN DJATHTAS EKRANIT-->
            <v-col class="card-container" cols="6">
                <v-row class="card-container" v-for="(item,index) in heroCards" :key="index">
                    <v-card
            color="#1F7087"
            
            class="card-style"
          >
            <div class="d-flex flex-no-wrap ">
                <v-avatar
                class="ma-0"
                size="185"
                rounded="0"
              >
                <v-img :src="item.image"></v-img>
              </v-avatar>
              <div>
                <v-card-title class="text-h5">
                  {{ item.title }}
                </v-card-title>
                <p class="description-style">{{ item.description }}</p>
                <!-- <v-card-subtitle>{{ item.description }}</v-card-subtitle> -->

                <v-card-actions>
                  <v-btn
                    class="ms-2"
                    variant="outlined"
                    size="small"
                  >
                    {{ item.button }}
                  </v-btn>
                </v-card-actions>
              </div>
            </div>
          </v-card>
                </v-row>
        
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
                    ],
                    heroCards:[
                        {
                            title:"Back in time with nintendo switch",
                            description:"Nintendo Switch është një sistem i suksesshëm dhe është përdorur nga lojtarë të të gjitha moshat në mbarë botën. Ai është një sistem i përshtatshëm, i dizajnuar për të përfshirë dhe për të ofruar mundësinë për të shijuar lojërat e Nintendo në çdo moment dhe kudo.",
                            button:'Detajet...',
                            image:require('@/assets/nintendo.png')
                        },
                        {
                            title:"Work with dual monitor !",
                            description:"Pse duhet te punoni me dual monitor? Dual monitorët e përmirësojnë produktivitetin duke ofruar më shumë hapësirë pune. Ky model pune lejon shikimin e dy dritareve të ndryshme njëkohësisht, duke përmirësuar organizimin e punës. Mundësia për të kryer multitasking më lehtë është një avantazh kryesor i punës me dual monitor.",
                            button:'Detajet...',
                            image:require('@/assets/doublemonitor.png')
                        },
                        {
                            title:"Latest razer keyboard !",
                            description:"Fjala e fundit e evolucionit të tastierës është këtu tek ne. Razer Huntsman Line përmban butonat e reja optike Razer™ Analoge Gen-2, duke siguruar aktivizim me shpejtësinë e dritës. ",
                            button:'Detajet...',
                            image:require('@/assets/keyboard.png')
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
        display: flex;
        flex-direction: row;
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

    @media only screen and (min-width: 1300px) {
    .col-category{
        
        margin-right: 20px;
        height: 91%;
    }
    .row-hero{
        padding-top: 440px;
        height: fit-content;
        background-color: #194554;

    }

    .categories-title-style{
        font-size: 18px;
        width: 231px;
    }
    .button-style{
        font-size: smaller;
    }

    .full-size {
    width: 100%;
    height: 95%;
    }

    .card-description {
    max-width: 700px;
    text-overflow: ellipsis; /* Add this line to display ellipsis for overflowed text */
    font-size: 12px;
    padding-left: 12px;
}
    .card-col{
        margin-right: 120px;
        margin-top: 20px;
     width:max-content;
    }

    }

    .description-style{
        font-size: 12px;
    }
/card-container{
    padding-left: 10px !important;
}

    </style>

