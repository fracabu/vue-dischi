<template>
  <div id="app">
    <TheHeader></TheHeader>
    <ListaDischi></ListaDischi>
    <TheDisco></TheDisco>
  
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import ListaDischi from './components/ListaDischi.vue'
import TheDisco from './components/Disco.vue'




export default {
  name: 'App',
  components: {
    TheHeader,
    ListaDischi,
    TheDisco
}
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
