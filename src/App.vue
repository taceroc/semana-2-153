<template>
  <div id="app">
    <div class="container-fluid">
      <h2 class="text-center text-white bg-dark" id="news">{{ titulo_noticias }}</h2>
      <NoticiaApi></NoticiaApi>
    </div>
  </div>
</template>

<script>
import NoticiaApi from "./components/NoticiaApi.vue";

export default {
  name: "App",
  components: {
    NoticiaApi,
  },
  data() {
    return {
      titulo_noticias: "Noticias",
    };
  },
};
</script>

