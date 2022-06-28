<template>
    <div class="py-5">
        <div class="alert alert-info">
            genere attivo :{{searchGenre}}
        </div>
        <div class="row row-cols-5 g-3">
            <div class="col" v-for="(album, i) in  filteredAlbums" :key="album.title + i">
                <AlbumCard :album="album"></AlbumCard>
            </div>
        </div>
    </div>
</template>

<script>
import axios from "axios";
import AlbumCard from "./AlbumCard.vue";

export default {
    props:{
        searchGenre : String,
    },
    data() {
        return {
            urlDischi: "https://flynn.boolean.careers/exercises/api/array/music",
            /**
             * @type{{author: string, genre: string,poster: string,title: string,year: string}[]}
             *
             */
            albumsList: []
        };
    },
    computed:{
        filteredAlbums(){
            if(!this.searchGenre){
                return this.albumsList;
            }
            return this.albumsList.filter((album)=>{
                return album.genre === this.searchGenre
            });
            },
        },
    

    methods: {
        fetchData() {
            axios.get(this.urlDischi)
                .then((resp) => {
                    this.albumsList = resp.data.response;

                    this.$emit("genresUpdated",this.listaGeneri())
                })
                .catch(() => {
                    alert("A causa di un problema l'operazione non è andata a buon fine");
                });
        },
        listaGeneri(){
            const lista = [];
            
            this.albumsList.forEach( album => {
                if(!lista.includes(album.genre)){
                    lista.push(album.genre)
                }
                
            });
            return lista
        }
    },
    mounted() {
        this.fetchData();
    },
    components: { AlbumCard }
};

</script>

<style lang="scss" scoped>
</style>