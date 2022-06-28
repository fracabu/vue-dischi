<template>
    <div class="d-flex">
        <div class="input-group">
            <select type="text" class="form-select">
                <option value="">scegli un genere</option>
                <option v-for="(genere, i) in listaGeneri" :key="i" value="genere">{{genere}}</option>
            </select>
            <button class="btn btn-primary"> Cerca</button>
        </div>

    </div>
</template>

<script>
export default{
    props:{
        listaGeneri : Array
    }
}

</script>

<style lang="scss" scoped>

.btn{
    background-color: #2E3A46;
}
</style>