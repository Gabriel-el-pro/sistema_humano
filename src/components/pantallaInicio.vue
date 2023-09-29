<template>
<v-main class="fondo">
<v-container >
    <v-row align="center" justify="center" style="height: 550px;" >
        <router-link to="/pantallaP" >
     <v-btn
      fab
      color="cyan"
      height="160"
      width="160"
      

    >
    
      <v-img
          src="../assets/iniciar.png"
          width="160"
          height="160"
          class="animation"
        ></v-img>
    </v-btn>
     </router-link>
  </v-row>
</v-container>
<h1>
   Intoxicación II
    </h1>
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

<style  scoped>
.fondo{
    background: url(../../public/fondo2.jpg) no-repeat center fixed;
   -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
 }
 h1{
   color:#fc5e4d;
 text-align: center;
 margin-top: -200px;
 font-size: 48px;
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
</style>