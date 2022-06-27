<template>
    <div class="album-card">
        <img :src="album.poster" alt="" class="album-img">
        <h5 class="text-white text-uppercase">{{album.title}}</h5>
        <small class="text-muted">{{album.author}}</small><br>
        <small class="text-muted">{{album.year}}</small>
    </div>
</template>

<script>
export default{
    props:{
        album:{
            type:Object,
            required: true,
        },      
    },
};

</script>

<style lang="scss" scoped>
.album-card{
    background-color: #2E3A46;
    padding: 1rem;
    text-align: center;
    height: 100%;
}

.album-img{
    width: 100%;
    aspect-ratio: 1/1;
    padding-bottom: 1rem;
}




</style>