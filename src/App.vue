<template>
  <div id="app">
    <banner-principal> </banner-principal>
  </div>

  <div class= "container-fluid">
  <div class= "row justify-content-center mb-5" >
    <div class="col mt-5" v-for="(item, index) of equipo" :key="index">
      <team-card v-bind:member="item"></team card>
    </div>
  </div>
</div>
</template>

<script>

import BannerPrincipal from "./components/BannerPrincipal.vue";
import TeamCard from './components/TeamCard.vue'

export default {
  name: 'App',
  components: {
  BannerPrincipal,
  TeamCard
  },
data(){
  return{
    title : 'Miembros en VUE',
    equipo: [
      {
        codigo: 1,
        nombre: "Iván Rodríguez",
        descripcion: "Soy ingeniero en tele-comunicaciones y estudiante de especialización en gestión de proyectos de ingeniería en la Universidad Distrital en Bogotá. En mi tiempo libre me gusta leer.",
        rol: "Desarrollador backend",
        image: "./equipoimagenes/IR.jpg",
      },
      {
        codigo: 2,
        nombre: "León Piedrahita",
        descripcion: "Estudié bioingeniería en la Universidad de Antioquia. Vivo en Itagüí. Me gusta salir a caminar con mi perro.",
        rol: "Arquitecto de software",
        image: "./equipoimagenes/LP.jpg",
      },
      {
        codigo: 3,
        nombre: "María Paola Gómez",
        descripcion: "Estudié ingeniería química y especialización en dirección de producción y operaciones en la Universidad Nacional de Colombia, Sede Manizales. Pertenezco al coro de dicha Universidad.",
        rol: "Tester",
        image: "./equipoimagenes/MG.jpg",
      },
      {
        codigo: 4,
        nombre: "Andrés Felipe Bedoya",
        descripcion: "Estudio ingeniería industrial en la Universidad de Ibagué. Generalmente, vivo en Ibagué, pero actualmente estoy en Chaparral. Me gusta hacer ruta en bicicleta y senderismo.",
        rol: "Analista",
        image: "./equipoimagenes/FB.jpg",
      },
      {
        codigo: 5,
        nombre: "Felipe Garavito",
        descripcion: "Soy comunicador audiovisual de la Universidad de La Sabana. Vivo en Bogotá. Mi hobby es hacer vudeojuegos.",
        rol: "Desarrollador Frontend",
        image: "./equipoimagenes/FG.jpg",
      }
    ]
  }
}
}
</script>

