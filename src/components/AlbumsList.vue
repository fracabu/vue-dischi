<template>
    <div class="py-5 container">
        <div class="row row-cols-5">
            <div class="col" v-for="(album, i) in albumsList" :key="i">
                <AlbumCard :album="album"></AlbumCard>
            </div>
        </div>
    </div>
</template>

<script>
import axios from "axios";
import AlbumCard from "./AlbumCard.vue";

export default {
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
    methods: {
        fetchData() {
            axios.get(this.urlDischi)
                .then((resp) => {
                    this.albumsList = resp.data.response;
                })
                .catch(() => {
                    alert("A causa di un problema l'operazione non è andata a buon fine");
                });
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