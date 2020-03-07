<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="music-cd">
    </div>
</template>

<!-- inserisco script  -->
<script>
// qui userò props perchè ricevo dati non sono miei

</script>

<!-- inserisco lo style tramite tag style
    attributo scoped mi restringe lo style a questo componente
    attributo lang gli dico che linguaggio sto usando
-->
<style lang="scss">
    //importo il file scss con le variabili
    @import "../../sass/_variables";
    .music-cd {
        background-color: lighten($backgound-color, 5%);
        min-width: 200px;
        min-height: 200px;
        margin: 20px;
    }
</style>
