<template>

    <div>
        <v-container  >
            <div class="container" >
       <div class="v-card v-sheet theme--light"  style="width: 810px; "  >
        <div  class="v-card__title headline " >
        <h1 >
          Primeros Auxilios -- Intoxicacion II</h1>
         
          </div>
          <hr  class="v-divider theme--light">
          <div  class="v-card__text">
        
        <div  class="layout column wrap align-center justify-center" style="position: relative; top: 30 px; left: 140px;   ">
        <div  >
        <iframe frameborder="0"
         allowfullscreen="1" 
         allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
         title="YouTube video player" width="470" height="300"
        src="https://www.youtube.com/embed/54pjH2putN4"
       
          >
          </iframe></div>
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
    data: () =>({
     //
    }),
}
</script>
<style scoped>
.headline{
text-align: center;
color: rgb(0, 0, 0);
text-shadow: 0px 2px 2px rgba(0, 0, 0, .2);
align-content: center;
font-size: 20px;



}
h2{
    text-align: center;
    color: rgb(25, 187, 187);
    text-shadow: 0px 2px 2px rgba(0, 0, 0, .2);
   align-content: center;
}
.v-card{
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  border-radius: 20px;
    background: url(../../public/tarjeta.jpg) ;
  
  background-size: cover;
 
}
.v-card:hover {
  box-shadow: 0 16px 32px 0 rgba(0,0,0,0.2);
}
iframe {
    border-radius: 60px ;
}





</style>


