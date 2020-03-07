<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html della mia app -->
    <div class="music-container">
        <!--
        - divido le parti della mia app in particelle e per ognuna creo un componente
        - creo la cartella components e al suo interno un file .vue per ogni componente
        - in ogni components.vue vado a definire template, script e style
        - importo i file dei componenti
            import MusicHeader from "../components/MusicHeader";
        - faccio export per attivare lo script del componente
            export default {
              components: {
                MusicHeader
              }
            };
        -->
        <music-header></music-header>
        <!-- il cds-container al suo interno avrà il singolo cd -->
        <music-cds-container></music-cds-container>
    </div>
</template>

<!-- inserisco script  -->
<script>
// importo i file dei componenti
import MusicHeader from "../components/MusicHeader";
import MusicCdsContainer from "../components/MusicCdsContainer";
//serve per usare lo script nel componente
export default {
  components: {
    MusicHeader,
    MusicCdsContainer
  }
};
</script>

<!-- inserisco lo style tramite tag style
    attributo scoped mi restringe lo style a questo componente
    attributo lang gli dico che linguaggio sto usando
-->
<style lang="scss">
    // importo il fiel con le variabili
    @import "../../sass/_variables";
    .music-container {
        width: 100vw;
        height: 100%;
        background-color: $backgound-color;
    }
</style>
