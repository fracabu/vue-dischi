<template>
    <div>
        {{ ListaDischi }}
        <div class="container">
            <div class="row row-cols-5" v-for="disco in ListaDischi" :key="disco.year">
                <div class="col mb-5">
                    <TheDisco></TheDisco>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
import axios from "axios"
import TheDisco from "./TheDisco.vue";


export default {
    name: "ListaDischi",
    components: { TheDisco },
    data() {
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            ListaDischi: [],
            loading: true,
        };
    },

    methods: {
        fetchListaDischi() {
            axios.get(this.apiURL).then((resp) => {

                this.ListaDischi = resp.data.response
            });
        },
    },
    mounted() {
        this.fetchListaDischi()

    }

};

</script>


<style>
body {
    background-color: #1E2D3B;
}
</style>