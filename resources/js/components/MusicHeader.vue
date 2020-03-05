<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="music-header">
        <div class="container">
            <div class="row">
                <div class="col-sm-4">
                    <span>Music Playlist</span>
                </div>
                <div class="col-sm-8">
                    <ul>
                        <li>Home</li>
                        <li>About us</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<!-- inserisco script  -->
<script>
// uso data() per passare variabili create da me
// inseriro data da passare a ciclo v-for su li

</script>

<!-- inserisco lo style tramite tag style
    attributo scoped mi restringe lo style a questo componente
    attributo lang gli dico che linguaggio sto usando
-->
<style lang="scss">

    $headerHeight: 70px;
    .music-header {
        background: lighten(#1d2d3b, 5%);
        height: $headerHeight;
        line-height: $headerHeight;
        color: white;
        ul {
            display: inline;
            list-style: none;
            text-align: right;
            li {
                display: inline-block;
            }
        }
    }

</style>
