<template>
  <div id="app">
    <NavBar></NavBar>
    <AlbumsList></AlbumsList>

  
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import AlbumsList from "./components/AlbumsList.vue";






export default {
  name: 'App',
  components: {NavBar,AlbumsList},
  data(){
    return{};
  },
  mounted(){},
};


</script>

<style lang="scss">
@import"./assets/main";
</style>
