
<template>
    <div>
        <v-container>
            
  <v-card
    class="mx-auto"
    width=" 810px"
    height="450px"
  >
    <v-card-text>
      <h3 class="v-card__title headline red lighten-5" >Actividad 1</h3>
      <h2>¿Qué causan las intoxicaciones dadas por ingestión?</h2>
      <br>
     <v-list>
       <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="models.base = true"
    >
      <v-list-item-title>Brote cutáneo comezón, irritación de ojos</v-list-item-title>

      <v-list-item-action>
        <v-icon :color="models.base ? 'red' : 'gray'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="models.base = true"
    >
      <v-list-item-title>Náuseas, vómitos, respiración y pulso débil, diarrea</v-list-item-title>

      <v-list-item-action>
        <v-icon :color="models.base ? 'green' : 'gray'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="models.base = true"
    >
      <v-list-item-title>Tos, agitación y fatiga</v-list-item-title>

      <v-list-item-action>
        <v-icon :color="models.base ? 'red' : 'gray'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     </v-list>
    </v-card-text>
    <br>
    <v-card-actions>
      <v-btn
           rounded
            large
        color="red accent-1"
        @click="reveal = true"
       
      >
        Siguiente
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <v-card
        v-if="reveal"
        class="transition-fast-in-fast-out v-card--reveal"
        height="100%"
       
      >
        <v-card-text class="pb-0" >
          <h3 class="v-card__title headline ">Actividad 2</h3>
          <p>pedro se tomó accidentalmente unos medicamentos que su mamá tenia, 
            arrastra las partes del cuerpo de pedro que serán afectadas  </p>
        <div class="ima">
           <div id="1" class="font" :style="{ backgroundImage:'url('+require('../assets/bazo.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
             <div id="2" class="font" :style="{ backgroundImage:'url('+require('../assets/boca.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
               <div id="3" class="font" :style="{ backgroundImage:'url('+require('../assets/cerebro.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
                 <div id="4" class="font" :style="{ backgroundImage:'url('+require('../assets/corazon.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
                   <div id="5" class="font" :style="{ backgroundImage:'url('+require('../assets/estomago.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
           <div id="6" class="font" :style="{ backgroundImage:'url('+require('../assets/igado.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
              <div id="7" class="font" :style="{ backgroundImage:'url('+require('../assets/ojos.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
                 <div id="8" class="font" :style="{ backgroundImage:'url('+require('../assets/pulmones.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
                    <div id="9" class="font" :style="{ backgroundImage:'url('+require('../assets/rinones.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
                       <div id="10" class="font" :style="{ backgroundImage:'url('+require('../assets/tripa.png')+')','background-size': '100% 100%', height:'40px',width:'40px',backgroundRepeat:'no-repeta',backgroundSize:'cover'}"  draggable="true" @dragstart="drag" @dragend="end"></div>
        </div>
         <div class="pelao">
           <div id="box-droppable" class="box-iner" @drop="drop" @dragover="allowDrop"> </div>
            <div id="box-droppable" class="box-iner2" @drop="drop" @dragover="allowDrop"> </div>
             <div id="box-droppable" class="box-iner3" @drop="drop" @dragover="allowDrop"> </div>
              <div id="box-droppable" class="box-iner4" @drop="drop" @dragover="allowDrop"> </div>
         </div>
         


    
 <v-tooltip bottom color="red"
          v-model="sh"
          top
          
        >
          <template v-slot:activator="{ on, attrs }">
            <label
            
              icon
              v-bind="attrs"
              v-on="on"
              
              >
            
            </label>
          </template>
          <span style="font-size:30px;color:blue;">Incorrecto</span>
        </v-tooltip>


    
        <v-tooltip bottom color="green"
          v-model="show"
          top
          
        >
          <template v-slot:activator="{ on, attrs }">
            <label
            
              icon
              v-bind="attrs"
              v-on="on"
              
              >
            
            </label>
          </template>
          <span style="font-size:30px;color:blue;">Correcto</span>
        </v-tooltip>
     

        </v-card-text>
        
      </v-card>
    </v-expand-transition>
  </v-card>

        </v-container>
    </div>



</template>
<script>
  export default {
    data: () => ({
      r:[],
      sh:false,
      show: false,
      reveal: false,
      models: {
        base: false,
        
      },
       
     
  
    }),
    methods: {
      impro(){
  this.r=[];
      this.sh=false;
      this.show= false;
      this.reveal= false;
      this.models= {
        base: false,
        
      };
      },
      cambio(){
this.show=false;
this.sh=false;
      },
        onDragging(ev){
      ev.dataTransfer.setData("text", ev.target.id);
      
    },
    allowDrop(ev) {
      ev.preventDefault();
     
    },
        end(ev){
	ev.target.style.opacity = ''; 	
	ev.dataTransfer.clearData("Data");			
},
    drag(ev) {
      ev.dataTransfer.setData("text", ev.target.id);
    },
    drop(ev) {
     ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  if(data==2||data==8||data==5||data==10){
this.show=true;
  }else{
this.sh=true;
  }
   setTimeout(this.cambio,2000);
   this.r.push(data);
  ev.target.appendChild(document.getElementById(data)); 
  if(this.r.length==4){
 setTimeout(this.impro,4000);
  }
    },
    },

       }
    
    
   
    
  
  
</script>
<style scoped>
.box-iner {
      margin: 5px;
         
         border-radius: 3px;
      display: flex;
    width:45px;
    height: 40px;
    padding: 1px;
    margin-top: 235px;
    margin-left:-185px;
  }
  .box-iner2 {
      margin: 5px;
         
         border-radius: 3px;
      display: flex;
    width:45px;
    height: 40px;
    padding: 1px;
    margin-top: -44px;
    margin-left:144px;
  }
  .box-iner3 {
      margin: 5px;
         
         border-radius: 3px;
      display: flex;
    width:45px;
    height: 40px;
    padding: 1px;
    margin-top: -176px;
    margin-left:175px;
  }
  .box-iner4 {
      margin: 5px;
        
         border-radius: 3px;
      display: flex;
    width:45px;
    height: 40px;
    padding: 1px;
    margin-top: -45px;
    margin-left:-229px;
  }
.ima{
  float:left;
max-width: 200px;
max-height:500px;
margin-left: 80px;
}
.font{
  float:left;
  
}
.ima2{
 float:right;
max-width: 200px;
height:200px;
border:2px solid red;
}
.pelao{
 
  margin-left: auto;
  
   width: 310px;
            height: 310px;
            background-image: url("../assets/pelao.png");
            background-size: 100% 100%;
            border-radius: 5px;
            border: 2px solid deeppink;
}
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
  
}
hr{
  height: 4px;
  background-color: black;
}
.v-btn{

          position:absolute;
         left:25%;
         top:67%;
         width:50%;
         


  
}

</style>

      

     