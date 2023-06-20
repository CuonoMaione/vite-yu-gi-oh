<template>
    <div class="card col-2 mb-3">

        <img :src="image" class="card-img-top" alt="...">

        <div class="card-body">
            <h5 class="card-title">{{ name }}</h5>
            <p class="card-text">{{ species }}</p>
        </div>
</div>
</template>

<script>

export default {
    name: 'CharacterCard',
    props:{
    name : String,
    species : String,
    image : String,
    }
}

</script>

<style scoped >
    img{
        width: 100%;
    }
</style>