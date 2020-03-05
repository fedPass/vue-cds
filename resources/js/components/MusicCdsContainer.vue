<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="">
        <div class="container">
            <!-- inserisco un componente dentro un componente -->
            <music-cd></music-cd>
        </div>
    </div>
</template>

<!-- inserisco script  -->
<script>
// uso data() per passare variabili create da me
//importo la componente
import MusicCd from "./MusicCd";

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
<style lang="scss">

</style>
