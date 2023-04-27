<template>
<v-main  class="fondo">
  <div class="container ">
 
    <div class="text-center d-flex align-center justify-space-around">
         <div >

<img src="../../public/doctor.png"  width="80" height="80">
<h2 class="display-1 mr-3 ">Intoxicación II</h2>
<hr>
</div>
    <v-tooltip bottom  color="red darken-1">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          fab
          v-bind="attrs"
          v-on="on"
          href="/"
          
         
        >
        <img src="../../public/hospital.png" width="95"  height="70" class="animation" >
        </v-btn>
      </template>
      <span  >Inicio</span>
      
      
      
    </v-tooltip>
    
     <v-tooltip bottom color="blue darken-2">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          
          fab
          v-bind="attrs"
          v-on="on"
          href="/introduccion"
        >
        <img src="../../public/prescripcion.png" width="70" class="animation">
        </v-btn>
      </template>
      <span>Contenido</span>
    </v-tooltip>
     <v-tooltip bottom color="#184D5F">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          fab
          v-bind="attrs"
          v-on="on"
          href="/actividades"
        >
        <img src="../../public/medicine-book.png" width="70" class="animation">
        </v-btn>
      </template>
      <span>Actividades</span>
    </v-tooltip>
     <v-tooltip bottom color="#FB7B6C">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          fab
          v-bind="attrs"
          v-on="on"
          href="/evaluacion"
        >
        <img  src="../../public/tareas.png" width="70"  class="animation">
        </v-btn>
      </template>
      <span>Evaluación</span>
    </v-tooltip>
     <v-tooltip bottom >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          fab
          v-bind="attrs"
          v-on="on"
          href="/creditos"
        >
        <img src="../../public/informacion.png" width="70" class="animation">
        </v-btn>
      </template>
      <span>Acerca de </span>
    </v-tooltip>

  </div>
  </div>
  
  

  <v-col align="center" justify="center">
       <router-view></router-view>
    </v-col>
 
</v-main>
  
   
    
    

</template>
<script>
export default {
    name:"App",
    data: () =>({
     //
    }),
}
</script>
<style scoped>
.fondo{
    
    background: url(../../public/imagen.jpg) no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
 }
 h2{
 text-shadow: 0px 2px 2px rgba(0, 0, 0, .4);
 }
.animation{
   animation-name: boton;
   animation-duration: .8s;
   animation-timing-function: linear;
   animation-iteration-count: infinite;
   animation-direction: alternate;
 }
 @-webkit-keyframes boton{0%{transform:scale(1);}to{transform: scale(1.1);}}
@keyframes boton{0%{transform:scale(1);}to{transform: scale(1.1);}}
hr {border-radius: 10px; width: 500%; height: 20px; box-shadow: inset 0 22px 12px -12px rgb(0, 0, 0); color: rgb(0, 0, 0); text-align: center;}

 

</style>

