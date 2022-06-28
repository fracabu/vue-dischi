<template>
  <div id="app">
    <NavBar :lista-generi = "listaGeneri" @searchGenre="onSearchGenre"></NavBar>

    <div class="container">
      <AlbumsList @genresUpdated="onGenresUpdate" :search-genre="searchGenre"></AlbumsList>
    </div>


  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import AlbumsList from "./components/AlbumsList.vue";






export default {
  name: 'App',
  components: { NavBar, AlbumsList },
  data() {
    return {
      //salvo localmente nel data la lista che ho ricevuto con l'emit per inoltrarla ad una prop nel componente NavBar
      // in modo che ogni volta che la variabile (listaGeneri) verrà modificata anche la prop verrà automaticamente
      // modificata
      listaGeneri:[],
      searchGenre:"",
    };
  },

  methods:{
    // funzione per leggere l'emit con la listageneri
    onGenresUpdate(listaGeneri){
      console.log(listaGeneri);
      this.listaGeneri = listaGeneri
    },

  onSearchGenre(genre){
    this.searchGenre = genre;

  }
  },
  mounted() { },
};


</script>

<style lang="scss">
@import"./assets/main";


#app{
  overflow: hidden;
  display: flex;
  flex-direction: column;
};

.container{
  overflow: auto;
}
</style>
