<template>


      <v-app id="app">
        
        <v-container>
         <v-row >
          <v-col
          v-for="card in cards"
          :key="card.titulo"   
          >
          <v-card  style="max-width: 344px; margin: 12px;" >
            <v-img :src= "card.src" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)" height="300px" cover >            
          </v-img>
          <v-card-title style="justify-content: center;">{{card.titulo}}</v-card-title>
          <v-card-subtitle>{{ card.subtitulo }}</v-card-subtitle>
          </v-card>

          </v-col>
         </v-row>
          

        </v-container>

      </v-app>


    </template>

  </v-app>

</template>

  <script>
  export default{
  data() {
    return {
      cards:
  [
  {
  titulo: "Martes 04/04", 
  subtitulo:"River vs The strongest",
  src: "https://www.elgrafico.com.ar/media/cache/pub_news_list_a/media/i/31/57/31578457a27b37030d55e370df138610a31ce43b.jfif",
  flex:"3"},
  {
  titulo: "Domingo 09/04", 
  subtitulo:"River vs Huracan",
  src: "https://media.tycsports.com/files/2021/08/01/314587/river-huracan_1440x810_wmk.jpg",
  flex:"3"},
  {
  titulo: "Jueves 13/04", 
  subtitulo:"River Gimnasia",
  src: "https://mirror1.cdn.net.ar/mirror1/mirror1/images/02/16/21674_4933ae092e6f9df254ede73aa8bb8d18ba9cf84324f7ab0f1874f429a8de0948/sm.webp",
  flex:"3"},
  {
  titulo: "Domingo 16/04", 
  subtitulo:"River vs Newells",
  src: "https://media.tycsports.com/files/2022/08/13/464951/pablo-perez-gol-newells-vs-river_862x485.webp?v=1",
  flex:"3"},
  {
  titulo: "Domingo 16/04", 
  subtitulo:"River vs Newells",
  src: "https://media.tycsports.com/files/2022/08/13/464951/pablo-perez-gol-newells-vs-river_862x485.webp?v=1",
  flex:"3"},
  
]
}
  }
  }
  
</script>

