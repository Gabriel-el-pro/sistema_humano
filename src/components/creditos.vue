<template>
    <div>
        <v-container>
            
<div class="v-dialog v-dialog--active" style="max-width: 400px;">
<div class="v-card v-sheet theme--light">
<div class="v-card__title  primary red accent-2 v-card__title--primary">
<h2 class="text-uppercase headline">Integrantes del Proyecto</h2>
</div>
<div class="v-card__text ">
<div role="list" class="v-list transparent theme--light">
<div role="listitem">
<div class="v-list__tile v-list__tile--avatar theme--light">
<div class="v-list__tile__content">
<div class="v-list__tile__title font-weight-bold">Ardwin Moreno Valderrama</div>
</div>
<div class="v-list__tile__avatar">
    <div class="v-avatar" style="height: 40px; width: 40px;">
    <img src="../../public/ardwin.jpg" @click="verArdwin()">
 </div>
 <v-dialog
            v-model="persona"
            :overlay="false"
            max-width="500px"
            transition="dialog-transition"
          >
            <v-card :img="info.avatar" width="500" height="500">
              
            </v-card>
          </v-dialog>
    </div>
     </div>
           </div>
<div role="listitem">  
<div class="v-list__tile v-list__tile--avatar theme--light">
<div class="v-list__tile__content">
<div class="v-list__tile__title  font-weight-bold">Aldair Delgado Sanchez</div>
</div>
<div class="v-list__tile__avatar">
 <div class="v-avatar" style="height: 40px; width: 40px;">
 <img src="../../public/aldair.jpg"  @click="verAldair()">
    </div>
    <v-dialog
            v-model="persona"
            :overlay="false"
            max-width="500px"
            transition="dialog-transition"
          >
            <v-card :img="info.avatar" width="500" height="500">
              
            </v-card>
          </v-dialog>
    </div>
    </div>
    </div>
<div role="listitem">
<div class="v-list__tile v-list__tile--avatar theme--light">
 <div class="v-list__tile__content">
 <div class="v-list__tile__title  font-weight-bold">Tatiana Jerónimo Montiel</div>
</div>
<div class="v-list__tile__avatar">
<div class="v-avatar" style="height: 40px; width: 40px;">
 <img src="../../public/tatiana.jpeg"  @click="vertatiana()">
     </div>
     <v-dialog
            v-model="persona"
            :overlay="false"
            max-width="500px"
            transition="dialog-transition"
          >
            <v-card :img="info.avatar" width="500" height="500">
              
            </v-card>
          </v-dialog>
     </div>
     </div>
     </div>
<div role="listitem">
 <div class="v-list__tile v-list__tile--avatar theme--light">
 <div class="v-list__tile__content">
 <div class="v-list__tile__title font-weight-bold">Yeison Pacheco </div>
 </div><div class="v-list__tile__avatar">
<div class="v-avatar" style="height: 40px; width: 40px;">
<img src="../../public/yeison.jpeg"  @click="veryeison()">
     </div>
     <v-dialog
            v-model="persona"
            :overlay="false"
            max-width="500px"
            transition="dialog-transition"
          >
            <v-card :img="info.avatar" width="500" height="500">
              
            </v-card>
          </v-dialog>
    </div> 
     </div>
     </div>
     <hr class="v-divider theme--light">
     <div role="listitem" class="primary red accent-2 mt-4">
     <div class="v-list__tile theme--light">
<div class="v-list__tile__content">
 <div class="v-list__tile__title">Docente: Aly Benhur C. De La Vega</div>
 </div><div class="v-list__tile__avatar">
 <div class="v-avatar" style="height: 40px; width: 40px;">
<img src="../../public/profesor.jpeg" @click="verAly()">
       </div>
       <v-dialog
            v-model="persona"
            :overlay="false"
            max-width="500px"
            transition="dialog-transition"
          >
            <v-card :img="info.avatar" width="500" height="500">
              
            </v-card>
          </v-dialog>
       </div>
       </div>
       </div>
 <div class="v-list__tile__content"> 
<img src="../../public/unicor.png" class="ml-4 mt-4" width="200px" height="80px">

                </div>
                </div>
                </div>
                </div>
                </div>
        </v-container>
    </div>
</template>
<script>
export default {
    name:"App",
    data: () =>{
       return {
      info: {},
      dialog: false,
      persona: false
    }
    },
    methods: {

    verAly () {
      this.info = {
        nombre: 'Aly Benhur Culchac De La Vega',
        avatar: require('../../public/profesor.jpeg')
      }
      this.persona = true
    },
    verArdwin () {
      this.info = {
        nombre: 'Ardwin moreno valderrama',
        avatar: require('../../public/ardwin.jpg')
      }
      this.persona = true
    },
     verAldair () {
      this.info = {
        nombre: 'Aldair delgado sanchez',
        avatar: require('../../public/aldair.jpg')
      }
      this.persona = true
    },
     vertatiana () {
      this.info = {
        nombre: 'tatiana jeronimo montiel',
        avatar: require('../../public/tatiana.jpeg')
      }
      this.persona = true
    },
     veryeison () {
      this.info = {
        nombre: 'yeison pacheco rangel',
        avatar: require('../../public/yeison.jpeg')
      }
      this.persona = true
    },
     
    
    

  },
}
</script>

 




