<template>
    <div class="card col-2 ms-4 mb-3 p-0">

        <img :src="image" class="card-img-top" alt="...">

        <div class="card-body">
            <h5 class="card-title text-white fw-bold text-center">{{ name }}</h5>
            <p class="card-text text-center">{{ species }}</p>
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
    div.card-body{
        background-color: #d48f38;
    }

    h5.card-title{
        
    }
</style>