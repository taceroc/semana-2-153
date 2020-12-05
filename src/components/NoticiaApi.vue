<template>
  <div class="row justify-content-center mt-1">
    <div
      class="col-sm-6 mb-3"
      v-for="(noticia, index) of noticias"
      v-bind:key="index"
    >
      <div class="card text-justify bg-light">
        <h2 class="noticias__card__title p-2">
          {{ noticia.title }}
        </h2>
        <div class="noticias__card__container text-center">
          <img
            class="card-img-top rounded mx-auto d-block"
            v-bind:src="noticia.image"
            alt="eganbernal"
          />
          <p class="p-2 text-justify">
           {{noticia.description}}
          </p>
          <a
            class="text-info text-decoration-none"
            v-bind:href="noticia.url"
            target="_blank"
            >Noticia completa</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
    name: "NoticiaApi",
    data(){
        return{
            noticias: null,
        };
    },
    mounted(){
         axios
      .get("https://gnews.io/api/v4/search?q=example&country=au&token=a8f4357881532af17f0324b5422963d7")
      .then((response) => {
        this.noticias = response.data.articles.slice(0,4);
        console.log(this.noticias);
      });
    },
};

</script>

<style scoped>
h2 {
    height: 120px;
    text-align: center;
    display: flex;
    align-items: center;
}

img{
    height: 290px;
    width: 560px;
}

</style>