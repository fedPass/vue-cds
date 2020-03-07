<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="music-cd">
        <!-- ho passato le info come props tramite l'attr :cd nel ciclo v-for -->
        <img :src="cd.poster" :alt="cd.title">
        <p><strong> {{ cd.title }} </strong></p>
        <p><em> {{ cd.author }} </em></p>
        <p> {{ cd.year }} </p>
    </div>
</template>

<!-- inserisco script  -->
<script>
// qui userò props perchè ricevo dati non sono miei
    export default {
      props: ["cd"]
    };
</script>

<!-- inserisco lo style tramite tag style
    attributo scoped mi restringe lo style a questo componente
    attributo lang gli dico che linguaggio sto usando
-->
<style lang="scss">
    //importo il file scss con le variabili
    @import "../../sass/_variables";
    .music-cd {
        text-align: center;
        background-color: lighten($backgound-color, 5%);
        width: 200px;
        height: 300px;
        margin: 20px;
        padding: 20px;
        color: $header-font-color;
        img {
            width: 100%;
            padding-bottom: 10px;
        }
    }
</style>
