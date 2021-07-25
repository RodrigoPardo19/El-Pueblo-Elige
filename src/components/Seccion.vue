<template>

      <div class="componenteGeneral">
        <div class="perfiles" >
          <div class= "img">
            <img src = "https://images.unsplash.com/photo-1536115706628-e1abad95f29a?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80" alt="">
          </div>
          <div class="textoSuperior" >
            <p> El único gobernador electo en un cupo de Chile Vamos analizó la situación de su región y fue crítico con la gestión de este y los anteriores gobiernos ante el conflicto en La Araucanía, la zona más pobre de Chile.
          </p>
          </div>
          <div class="textoIntermedio" >
            <p> Loli Guacamayo , gobernador electo en La Araucanía: “A la política le falta conectarse con sus territorios y con la gente”
          </p>
          </div>
          <div class="textoInferior" >
            <p> Todos esos espacios que ha dejado el Estado, son caldo de cultivo para que lleguen grupos vinculados al narcotráfico y la violencia y que exceden al tema indígena que es con lo que se trata de mezclar: la violencia con el mundo mapuche y es lo más injusto que se ha hecho".
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
.componenteGeneral{
  position: relative;
}

.perfiles{
  background-color: rgb(255, 255, 255);
  color: rgb(2, 1, 1);
  width: 900px;
  height:300px;
  border-radius: 2%;
  position: relative;
  left: 0px;
  top: 30px;
}

.textoSuperior {
  text-align: left;
  width: 70%;
  height: 30%;
  position: absolute;
  left: 270px;
  top: 0px;
}
.textoIntermedio {
  text-align: left;
  width:70%;
  height:30%;
  position:absolute;
  left:270px; 
  top: 80px;
}
.textoInferior {
  text-align: left;
  width:70%;
  height:20%;
  position:absolute;
  left:270px; 
  top: 180px;
}

.boton3{
   position:absolute;
   left:510px; 
   top: 260px;
}
img {
  width: 250px;
  height: 280px;
  image-rendering: optimizeQuality;
  object-fit: cover;
  border-radius: 7%;
  position: absolute;
  left: 10px;
  top: 10px;
}
</style>
