<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html della mia app -->
    <div class="music-container">
        <!--
        - divido le parti della mia app in particelle e per ognuna creo un componente
        - creo la cartella components e al suo interno un file .vue per ogni componente
        - in ogni components.vue vado a definire template, script e style
        - importo i file dei componenti
            import MusicHeader from "../components/MusicHeader";
        - ???
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

export default {
  components: {
    MusicHeader
  }
};
</script>

<!-- inserisco lo style tramite tag style
    attributo scoped mi restringe lo style a questo componente
    attributo lang gli dico che linguaggio sto usando
-->
<style lang="scss">
    .music-container {
        width: 100vw;
        height: 100vh;
        background-color: #1d2d3b;
    }
</style>
