<template>
  <div id="app">
    <div class="container-fluid text-center">
        <h2 id="team" class="text-center text-white bg-dark">
          Integrantes grupo 153
        </h2>
      <div class="row justify-content-center mb-3 mt-0">
        <div
          class="col-sm-6 col-xs-12 col-lg-3 mt-5"
          v-for="(item, index) of team"
          v-bind:key="index"
        >
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TeamCard from "./components/TeamCard.vue";

export default {
  name: "App",
  components: { TeamCard },
  data() {
    return {
      team: [
        {
          codigo: 1,
          nombre: "Tatiana Acero Cuellar",
          descripcion:
            "Estudiante de Física. Universidad Nacional de Colombia. 22 años. Pasatiempo: Ver anime.",
          rol: "Desarrollador backend",
          image:require('./assets/Tatiana.png')
        },
        {
          codigo: 2,
          nombre: "Cristian Camilo Parra Parra",
          descripcion:
            "Ingeniero Industrial. Universidad de Cundinamarca. 27 años. Pasatiempo: Viajar.",
          rol: "Desarrollador backend",
          image: require('./assets/Camilo.png'),
        },
        {
          codigo: 3,
          nombre: "Daniel Picon Agudelo",
          descripcion:
            "Estudiante de Ingenieria en Computacion. 19 años. Pasatiempo: Jugar videojueos.",
          rol: "Desarrollador backend",
          image: require('./assets/Daniel.png'),
        },
        {
          codigo: 4,
          nombre: "Hanssel Neira",
          descripcion:
            "Estudiante de ingeniería en control y automatización. Universidad Distrital. Amante del baloncesto. Lectura de cómics.",
          rol: "Desarrollador backend",
          image: require('./assets/Hansell.png'),
        },
      ],
    };
  },
};
</script>