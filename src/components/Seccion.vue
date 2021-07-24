<template>
  <div class="seccion">
    <h1>Entrevistas +</h1>
  </div>
<div class="componenteGeneral">
  <div class="perfiles" >
    <div class= "img">
      <img src = "https://images.unsplash.com/photo-1536115706628-e1abad95f29a?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80" alt="">
    </div>
    <div class="textoSuperior" >
      <p> Bienvenidos a la presentacion de los candidatos
    </p>
    </div>
    <button class="boton1">Editar</button>
    <div class="textoIntermedio" >
      <p> Loli Guacamayo , Candidato a Gobernante 
    </p>
    </div>
    <button class="boton2">Editar</button>
    <div class="textoInferior" >
      <p> Bienvenidos a la presentacion de los candidatos, esta es la seccion numero 3
    </p>
    </div>
    <button class="boton3">Editar</button>
  </div>
  </div>
</template>

<script>
export default {
  name: "Seccion",
};
</script>

<style scoped>
.seccion {
  text-align: left;
}
.perfiles{
  background-color: rgb(185, 184, 184);
  color: rgb(2, 1, 1);
  width: 500px;
  height:300px;
  border-radius: 7%;
  position: relative;
  left: 10px;
  top: 90px;
}

.textoSuperior {
  text-align: center;
  width: 50%;
  height: 50%;
  position: absolute;
  left: 210px;
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
  text-align: center;
  width:90%;
  height:50%;
  position:absolute;
  left:10px; 
  top: 180px;
}
.boton1{
  position:absolute;
   left:310px; 
   top: 60px;
   color: rgb(255, 255, 255);
}
.boton2{
  position:absolute;
   left:310px; 
   top: 150px;
}
.boton3{
   position:absolute;
   left:230px; 
   top: 250px;
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
