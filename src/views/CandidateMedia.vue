<template>
<body >
<div><NavBar /></div>
<div><SideBar /></div>
<div class="Seccion">
  <v-container>
    <v-row v-for="n in 2" :key="n" sm="9">
          <p>
          <Seccion/>
          </p>
    </v-row>
  </v-container>
</div>
<div class="texto">
    <h1>Entrevistas +</h1>
  </div>
  </body>
</template>
<script>

import NavBar from "@/components/NavBar.vue";
import SideBar from "@/components/SideBar.vue";
import Seccion from "@/components/Seccion.vue";


export default {
  name: "CandidateMedia",
  components: {
    NavBar,
    SideBar,
    Seccion,    
  },
};
</script>
<style scoped>

body{
background-color:#F3F1F1;
}
.Seccion{
  position: absolute;
  top: 100px;
  left: 300px;
}
.texto {
  position: absolute;
  text-align: left;
  top: 50px;
  left: 300px;
}
</style>