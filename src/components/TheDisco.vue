<template>
    <div class="disco text-center">
        <img class="img-fluid" :src="info.author" :alt="info.title">
    <h4>i{{info.author}}</h4>
    <div>{{info.genre}}</div>
    </div>
</template>


<script>
export default{
    name: 'TheDisco',
    props: {
        info: Object
    }

}
</script>


<style>
</style>
