<template>
    <div class="container-lg bg-white py-5">
    <div class="row justify-content-center">
    <div class="col-11 ms-3 bg-dark text-white p-3" v-text="characterList.length==0?'Select archetype and click on Search':` found ${characterList.length} card`"> </div>
    <CharacterCard v-for="character in characterList" 
    :name="character.name"
    :species="character.archetype"
    :image="character.card_images[0].image_url"/>
    </div>
    </div>    
</template>

<script>
import CharacterCard from './CharacterCard.vue';


export default {
    name: "CharacterList",
    components: { CharacterCard, },
    props:{
        characterList : Array,
    },

    data() {
        return{
            
        }
    },    
    

};

   

</script>
<style>
    
</style>