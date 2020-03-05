<template>
    <!-- template può avere solo un figlio, al suo interno scrivo struttura html della mia app -->
    <div>
        <!--
        - divido le parti della mia app in particelle e per ognuna creo un componente
        - creo la cartella components e al suo interno un file .vue per ogni componente
        - 
        -->
        <music-header></music-header>
        <!-- il cds-container al suo interno avrà il singolo cd -->
        <music-cds-container></music-cds-container>
    </div>
</template>
