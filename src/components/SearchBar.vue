<template>
    <div class="d-flex">
        <div class="input-group">
            <select type="text" class="form-select" v-model="genre">
                <option value="">scegli un genere</option>
                <option v-for="(genere, i) in listaGeneri" :key="i" value="genere">{{genere}}</option>
            </select>
            <button class="btn btn-primary" @click="onSearchClick"> Cerca</button>
        </div>

    </div>
</template>

<script>
export default{
    props:{
        listaGeneri : Array,
    },
    data(){
        return{
            genre:[]
        }
    },
    methods:{
        onSearchClick(){
            this.$emit("searchGenre" , this.genre);
        },
    },
};

</script>

<style lang="scss" scoped>

.btn{
    background-color: #2E3A46;
}
</style>