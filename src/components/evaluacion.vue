<template>
    <div>
        <v-container>
            <v-card
    class="mx-auto"
    width=" 810px"
    height="450px"
  >
    <v-card-text v-if="pantalla==1">
      <h3 class="v-card__title headline green lighten-2" >Evaluacion</h3>
      <h2>¿Qué es la intoxicación?</h2>
      <br>
     <v-list>
       <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta(1)"
    >
      <v-list-item-title>Es una reacción fisiológica. </v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta1==1 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta(2)"
    >
      <v-list-item-title>Es la reacción del organismo ante el contacto con cualquier sustancia tóxica.</v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta1==2 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta(3)"
    >
      <v-list-item-title>Es una reacción o respuesta inmunitaria a sustancias que generalmente no son dañinas.</v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta1==3 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     </v-list>
    </v-card-text>
    <br>


     <v-card-text v-if="pantalla==2">
      <h3 class="v-card__title headline green lighten-2" >Evaluacion</h3>
      <h2>¿Cuál puede ser causa de una intoxicación?</h2>
      <br>
     <v-list>
       <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta_2(1)"
    >
      <v-list-item-title>Consumo de alimentos vencidos. </v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta2==1 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta_2(2)"
    >
      <v-list-item-title>Mala alimentación. </v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta2==2 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta_2(3)"
    >
      <v-list-item-title>Exceso de vitaminas. </v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta2==3 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     </v-list>
    </v-card-text>



     <v-card-text v-if="pantalla==3">
      <h3 class="v-card__title headline green lighten-2" >Evaluacion</h3>
      <h2>¿Clasificación de los tóxicos?</h2>
      <br>
     <v-list>
       <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta_3(1)"
    >
      <v-list-item-title>Minerales, vegetales y animales.  </v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta3==1 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta_3(2)"
    >
      <v-list-item-title>Gases, líquido y sólidos. </v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta3==2 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     <v-list-item
      v-click-outside="{
        handler: onClickOutsideStandard,
        include: include,
      }"
      @click="pregunta_3(3)"
    >
      <v-list-item-title>Productos domésticos y agrícolas. </v-list-item-title>

      <v-list-item-action>
        <v-icon :color="pregunta3==3 ? 'green' : 'red'">
          mdi-record
        </v-icon>
      </v-list-item-action>
    </v-list-item>
     </v-list>
    </v-card-text>





 <v-card-text v-if="pantalla==4">
      <h3 class="v-card__title headline green lighten-2" >Evaluacion</h3>
      <h2>Relaciona las intoxicaciones con sus síntomas. Selecione primero la intorxicacion y luego el sintoma.</h2>
      <div class="yo">
        <a>  <div class="keti"  @click="pato1()">Inhalación</div></a>
           <a><div class="keti" @click="pato2()">Por piel</div></a>
          <a> <div class="keti" @click="pato3()">Ingestión </div></a>
      </div>
      <svg height="300" width="110" >
<line v-if="linea1==1"  x1="0" y1="70" x2="500" y2="60" style="stroke:blue;stroke-width:7" />
<line v-if="linea1==2" x1="0" y1="70" x2="500" y2="390" style="stroke:blue;stroke-width:7" />
<line v-if="linea1==3" x1="0" y1="70" x2="500" y2="780" style="stroke:blue;stroke-width:7" />

<line v-if="linea2==1"  x1="0" y1="155" x2="500" y2="-260" style="stroke:green;stroke-width:7" />
<line v-if="linea2==2" x1="0" y1="155" x2="500" y2="140" style="stroke:green;stroke-width:7" />
<line v-if="linea2==3" x1="0" y1="155" x2="500" y2="500" style="stroke:green;stroke-width:7" />

<line v-if="linea3==1"  x1="0" y1="240" x2="500" y2="-560" style="stroke:red;stroke-width:7" />
<line v-if="linea3==2" x1="0" y1="240" x2="500" y2="-170" style="stroke:red;stroke-width:7" />
<line v-if="linea3==3" x1="0" y1="240" x2="500" y2="220" style="stroke:red;stroke-width:7" />
      </svg>
      <div class="tu">
         <a>  <div class="cosa" @click="pato(1)">dolor de cabeza, visión borrosa y sudoración excesiva, confusión mental y muerte. </div></a>
         <a>    <div class="cosa" @click="pato(2)">quemaduras alrededor de la boca, náuseas, vómitos y diarrea </div></a>
         <a>  <div class="cosa" @click="pato(3)">brote cutáneo, irritación, comezón de ojos, trastornos auditivos y visuales. </div></a>
    
      </div>


<v-row justify="center">
    <v-dialog
      v-model="dialog"
      persistent
      max-width="350"
      
    >
      
      <v-card>
        
<v-tex  style="color:green;font-size:40px">Su nota es:<label> {{nota}}</label></v-tex>
       <v-card-actions>
          <v-spacer></v-spacer>
         
          <v-btn 
             color="blue accent-1"
        @click="reinicia()"
       style="position:absolute;
         left:25%;
         top:67%;
         width:50%;"
          >
           <h2> Aceptar</h2>
          </v-btn>
          
        </v-card-actions>
        
      </v-card>
    </v-dialog>
  </v-row>
<v-card-actions>
          <v-spacer></v-spacer>
         
          <v-btn 
             color="green accent-1"
        @click="nota_f()"
       style="position:absolute;
         left:25%;
         top:67%;
         width:50%;
         margin-top:110px"
          >
           <h2>Enviar</h2>
          </v-btn>
          
        </v-card-actions>
    </v-card-text>

    <v-card-actions v-if="pantalla<4">
      <v-btn
           rounded
            large
        color="red accent-1"
        @click="pantalla+=1"
       style="position:absolute;
         left:25%;
         top:67%;
         width:50%;"
      >
        Siguiente
      </v-btn>
    </v-card-actions>


  </v-card>
        </v-container>
       
    </div>
</template>
<script>
export default {
    name:"App",
    data: () =>({
        dialog:false,
        linea1:null,
        l1:false,
        linea2:null,
        l2:false,
        linea3:null,
        l3:false,
        pantalla:1,
      pregunta1:null,
      pregunta2:null,
      pregunta3:null,
      nota:0,
      models: {
        base: false,
        }
    }),
    methods: {
      reinicia(){
 this.dialog=false;
        this.linea1=null;
        this.l1=false;
        this.linea2=null;
        this.l2=false;
        this.linea3=null;
        this.l3=false;
        this.pantalla=1;
      this.pregunta1=null;
      this.pregunta2=null;
      this.pregunta3=null;
      this.nota=0;
      this.models= {
        base: false,
        }
      },
      nota_f(){
      if(this.pregunta1==2){
        this.nota+=0.5;
      }
       if(this.pregunta2==1){
        this.nota+=0.5;
      }
       if(this.pregunta3==1){
        this.nota+=1;
      }
       if(this.linea1==3){
        this.nota+=1;
      }
       if(this.linea2==1){
        this.nota+=1;
      }
       if(this.linea3==2){
        this.nota+=1;
      }
      this.dialog=true;
      },
        pato1(){
this.l1=true;
        },
         pato2(){
this.l2=true;
        },
         pato3(){
this.l3=true;
        },
        pato(p){
          if(this.l1==true){
this.linea1=p;
this.l1=false;
          }
           if(this.l2==true){
this.linea2=p;
this.l2=false;
          }
           if(this.l3==true){
this.linea3=p;
this.l3=false;
          }
         
        },
        pregunta(p){
         this.pregunta1=p;
        },
         pregunta_2(p){
         this.pregunta2=p;
        },
        pregunta_3(p){
         this.pregunta3=p;
        }
    },
}
</script>
<style>
    .yo{
        float:left;

max-width: 300px;
height:300px;
    }
    .tu{
 float:right;

max-width: 500px;
height:300px;
    }
    .keti{
        font-size:30px;
        width: 160px;
        max-height:50px;
        border-radius:20px;
        margin-top:60px;
        background-color: rgba(165, 42, 42, 0.39);
    }
    .cosa{
font-size:20px;
        width: 500px;
        max-height:50px;
        border-radius:20px;
        margin-top:40px;
        background-color: rgba(238, 171, 171, 0.39);
    }
</style>