<template>
<nav class="nav">
    <img :src="require('../assets/spotify-logo.png')" alt="" class="py-2 px-2">

    <SearchBar class="ms-auto" :lista-generi="listaGeneri"></SearchBar>
</nav>
    
</template>

<script>
import SearchBar from "./SearchBar.vue";
export default{
    components:{SearchBar},
    props:{
        listaGeneri : Array

    }
    
    
    };


</script>

<style scoped lang="scss">


.nav {
    background-color:#2E3A46 ;
    
}

</style>