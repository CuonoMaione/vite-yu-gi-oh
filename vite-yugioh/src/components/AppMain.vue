<template>
    <main class="p-5">
        <SearchBar @searched="showMyValue" />
        <CharacterList :characterList="characterList"/>
        
    </main>
</template>
<script>
import CharacterList from './CharacterList.vue';
import axios from 'axios';
import SearchBar from './SearchBar.vue';
export default {
    name: 'AppMain',
    components:{
        CharacterList,
        SearchBar,
    },
    data(){
        return{
            characterList: [],
            apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=40&offset=0'
        }
    },

    methods: {
        showMyValue(archetypeSelected){
            alert(archetypeSelected)
        }
    },

    created(){

    axios.get(this.apiUrl)
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