<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html-->
    <div class="music-header sticky-top">
        <div class="container">
            <div class="row">
                <div class="col-logo col-6">
                    <span><strong><a href="#">Music Playlist</a></strong></span>
                </div>
                <div class="sticky-menu col text-right">
                    <span><i class="fas fa-bars"></i></span>
                    <ul>
                        <li v-for="(link, index) in links" :key="index">
                            <a :href="link.href">{{ link.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-menu col text-right">
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
    //importo il file scss con le variabili
    @import "../../sass/_variables";
    .music-header {
        background-color: lighten($backgound-color, 5%);
        height: $headerHeight;
        line-height: $headerHeight;
        font-size: 20px;
        a {
            text-decoration: none;
            color: $header-font-color;
        }
        .col-logo {
            strong {
                text-transform: uppercase;
            }
        }
        .sticky-menu {
            position: relative;
            color: $header-font-color;
            ul {
                &.active {
                    display:block;
                }
                display: none;
                background-color: lighten($backgound-color, 20%);
                position: absolute;
                width: max-content;
                list-style: none;
                padding: 0;
                margin:0;
                right: 25px;
                li {
                    display: list-item;
                    margin: 0 20px;
                }
            }
            span{
                padding: 20px;
            }

        }
        .col-menu {
            display: none;
            color: $header-font-color;
            ul {
                list-style: none;
                li {
                    display: inline-block;
                    margin: 0 20px;
                }
            }
        }
    }

    @media (min-width: 992px) {
        .sticky-menu {
            display:none;
        }
        .col-menu {
            display: block;
        }
    }

</style>
