<template>
    <main class="p-5">
    
        <CharacterList/>
        
    </main>
</template>
<script>
import CharacterList from './CharacterList.vue';


export default {
    name: 'AppMain',
    components:{
        CharacterList,
        
    }
}
</script>
<style scoped>   
main{
    background-color: #d48f38;
} 
</style>