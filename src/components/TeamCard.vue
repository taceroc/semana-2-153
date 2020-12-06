<template>
    <div>
        <div class="card text-justify text-light bg-secondary">
          <img class="card-img-top img-flex rounded mx-auto" alt="Fotografia del miembro" v-bind:src="member.image"/>
          <div class="card-body">
            <h5 class="card-title text-center">{{member.nombre}}</h5>
            <p class="card-text"><span>Código:</span> {{member.codigo}}</p>
            <p class="card-text">{{member.descripcion}}</p>
            <p class="card-text ">{{member.rol}}</p>
        </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

.card-title{
    height: 48px;
}
.card-img-top{
    height: 260px;
    width: 240px;
    margin-top: 3px;
}


</style>
