<template>
  <div id="app">
    <NavBar></NavBar>

    <div class="container">
      <AlbumsList></AlbumsList>
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
    return {};
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
