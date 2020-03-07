<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="container">
        <div class="music-cds-container d-flex justify-content-center align-items-center flex-wrap">
            <!-- inserisco un componente dentro un componente
                dovrò ciclarlo per disegnare tutti i cds-->
            <music-cd></music-cd>
            <music-cd></music-cd>
            <music-cd></music-cd>
            <music-cd></music-cd>
            <music-cd></music-cd>
            <music-cd></music-cd>
        </div>
    </div>
</template>

<!-- inserisco script  -->
<script>
// uso data() per passare variabili create da me
//importo la componente
import MusicCd from "./MusicCd";
//per usare lo script nel componente
export default {
  components: {
    MusicCd
  }
};
</script>

<!-- inserisco lo style tramite tag style
    attributo scoped mi restringe lo style a questo componente
    attributo lang gli dico che linguaggio sto usando
-->
<style lang="scss" scoped>
    //importo il file scss con le variabili
    @import "../../sass/_variables";
    .container {
        padding-top: $headerHeight / 2;
    }
</style>
