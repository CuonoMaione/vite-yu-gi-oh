<template>
    <div class="container-lg">
    <div class="row">
    <CharacterCard v-for="character in CharacterList" 
    :name="character.name"
    :species="character.archetype"
    :image="character.card_images[0].image_url"/>
    </div>
    </div>    
</template>

<script>
import CharacterCard from './CharacterCard.vue';
import axios from 'axios';

export default {
    name: "CharacterList",
    component: {
        CharacterCard,
    },
    components: { CharacterCard, },

    data() {
        return{
            CharacterList : [],
        }
    },    
    created(){

    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
    .then( (response) => {
        console.log(response.data.data[0].card_images[0].image_url)
        this.CharacterList = response.data.data 
        
    })
    },

};

   

</script>
<style>
    
</style>