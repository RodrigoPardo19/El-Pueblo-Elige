<template>

<div class="seccion">
    <h1>Entrevistas  +</h1>
  </div>
<div class="componenteGeneral">
  
  <div class="perfiles" >
    <div class= "img">
      <img src = "https://images.unsplash.com/photo-1536115706628-e1abad95f29a?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80" alt="">
    </div>
    <div class="textoSuperior" >
      <p> Bienvenidos a la presentacion de los candidatos, esta es la seccion numero 1
    </p>
    </div>
    <div class="textoIntermedio" >
      <p> Bienvenidos a la presentacion de los candidatos, esta es la seccion numero 2
    </p>
    </div>
    <div class="textoInferior" >
      <p> Bienvenidos a la presentacion de los candidatos, esta es la seccion numero 3
    </p>
    </div>
  </div>
</div>
  
</template>
<style scoped>

.seccion {
  text-align: left;
}
.perfiles{
  background-color: rgb(243, 243, 243);
  color: rgb(2, 1, 1);
  width: 500px;
  height:300px;
  border-radius: 20%;
  position: relative;
  left: 10px; 
  top: 90px;
  
}

.textoSuperior {
  text-align: center;
  width:50%;
  height:50%;
  position:absolute;
  left:210px; 
  top: 0px;

}
.textoIntermedio {
   text-align: center;
  width:50%;
  height:50%;
  position:absolute;
  left:210px; 
  top: 80px;

}
.textoInferior {
  text-align: left;
  width:90%;
  height:50%;
  position:absolute;
  left:10px; 
  top: 180px;

}
img {
  width: 200px;
  height: 230px;
  image-rendering: optimizeQuality;
  object-fit: cover;
  border-radius: 20%;
  position: absolute; 
  left: 0px; 
  top: -90px;
}
</style>

