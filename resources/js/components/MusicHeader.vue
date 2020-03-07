<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="music-header">
        <div class="container">
            <div class="row">
                <div class="col-sm-4">
                    <span><strong>Music Playlist</strong></span>
                </div>
                <div class="col-sm-8">
                    <ul>
                        <!-- v-for per ciclo for in vue
                            uso la formula "singolare in plurale"
                            gli passo index e @key per evitare errore di compilazione
                        ( prende i dati da data() in script )-->
                        <li v-for="(link, index) in links" :key="index">
                            <!-- usiamo :href per specificare che el contiene una variabile -->
                            <a :href="link.href">{{ link.title }}</a>
                        </li>
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
export default {
data() {
    return {
        links: [
            { href: 'home', title: 'Home'},
            { href: 'about-us', title: 'About us'}
        ]
    }
}
}

</script>

<!-- inserisco lo style tramite tag style
    attributo scoped mi restringe lo style a questo componente
    attributo lang gli dico che linguaggio sto usando
-->
<style lang="scss">

    $headerHeight: 70px;
    $font-color: white;
    .music-header {
        background: lighten(#1d2d3b, 5%);
        height: $headerHeight;
        line-height: $headerHeight;
        color: $font-color;
        font-size: 20px;
        strong {
            text-transform: uppercase;
        }
        ul {
            list-style: none;
            text-align: right;
            li {
                display: inline-block;
                margin: 0 15px;
                a{
                    color: $font-color;
                }
            }
        }
    }

</style>
