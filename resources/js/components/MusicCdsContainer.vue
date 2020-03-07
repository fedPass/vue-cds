<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="container">
        <div class="music-cds-container d-flex justify-content-center align-items-center flex-wrap">
            <!-- inserisco un componente dentro un componente
                dovrò ciclarlo per disegnare tutti i cds
                prendo cds da ciclare dal array popolata da chiamata axios
                uso l'attributo :cd per passare come props al componente che lo disegna-->
            <music-cd v-for="(cd, index) in cds" :key="index" :cd="cd"></music-cd>
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
    },
    // data sono i dati che passerò io al v-for per disegnare i cd, è un array vuoto il cui pusherò i cds ricevuti tramite chiamata axios
    data() {
        return {
            cds: [],
        };
    },
    // muonted si usa per creare un componente
    //faremo chiamata axios per ricevere lista cds
    mounted() {
        //usiamo let così a valore soltanto in questa funzione
        //essendo due funzioni diverse useremo self per tirare i dati fuori dalla chiamata
        let self = this;
        //chiamata ajax  in vue -> axios
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then(function(response) {
                //dot notation -Z dipende dalla struttura del json
              self.cds = response.data.response;
            });
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
