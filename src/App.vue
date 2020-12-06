<template>
  <div id="app">
    <div class="container-fluid text-center">
        <h2 class="text-center text-white bg-dark">
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
            "Lorem ipsum dolor sit amet, consectetur adipiscingelit. Mauris condimentum ac elit et accumsan.",
          rol: "Desarrollador backend",
          image:require('./assets/Tatiana.png')
        },
        {
          codigo: 2,
          nombre: "Cristian Camilo Parra Parra",
          descripcion:
            "Lorem ipsum dolor sit amet, consectetur adipiscingelit. Mauris condimentum ac elit et accumsan.",
          rol: "Desarrollador backend",
          image: require('./assets/Camilo.png'),
        },
        {
          codigo: 3,
          nombre: "Daniel Picon Agudelo",
          descripcion:
            "Lorem ipsum dolor sit amet, consectetur adipiscingelit. Mauris condimentum ac elit et accumsan.",
          rol: "Desarrollador backend",
          image: require('./assets/Daniel.png'),
        },
        {
          codigo: 4,
          nombre: "Hanssel Neira",
          descripcion:
            "Lorem ipsum dolor sit amet, consectetur adipiscingelit. Mauris condimentum ac elit et accumsan.",
          rol: "Desarrollador backend",
          image: "path/to/image",
        },
      ],
    };
  },
};
</script>