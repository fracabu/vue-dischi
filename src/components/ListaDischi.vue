<template>
    <div>  
        {{ListaDischi}}
        <div class="container">
            <div class="row">
                <div class="col"></div>
                <div class="col-2 text-white">lista dischi</div>
                <div class="col-2 text-white">lista dischi</div>
                <div class="col-2 text-white">lista dischi</div>
                <div class="col-2 text-white">lista dischi</div>
                <div class="col-2 text-white">lista dischi</div>
                <div class="col"></div>
            </div>
        </div>
    </div>
</template>


<script>
import axios from "axios"


export default {
    name: "ListaDischi",
    components: {},
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

                this.ListaDischi = resp.data.results
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