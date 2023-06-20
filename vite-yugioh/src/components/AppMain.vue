<template>
    <main class="p-5">
    
        <CharacterList :characterList="characterList"/>
        
    </main>
</template>
<script>
import CharacterList from './CharacterList.vue';
import axios from 'axios';

export default {
    name: 'AppMain',
    components:{
        CharacterList,
        
    },

    data(){
        return{
            characterList: [],
        }
    },

    created(){

    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=40&offset=0')
    .then( (response) => {
    console.log(response.data.data[0].card_images[0].image_url)
    this.characterList = response.data.data 
    
})
},
}
</script>
<style scoped>   
main{
    background-color: #d48f38;
} 
</style>