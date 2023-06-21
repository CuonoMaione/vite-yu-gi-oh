<template>
    <div class="container-lg">
        <div class="row">
            <div class="col-5">
                <div class="input-group mb-3">
                    <select class="form-select" id="inputGroupSelect01" placeholder="Select archetype" v-model="archetypeSelected" @click="$emit('searched',archetypeSelected)">
                    <option v-for="index in archetypeList">{{ index }}</option>
                    </select>
                </div>
            </div>
        </div>
    </div> 
</template>
<script>
export default {
    name : 'SearchBar',
    data() {
        return {
            archetypeList : ['Select archetype','Alien','"C"','A.I.','Ignister','Dark Magician',"Aether",'Dragonmaid'],
            archetypeSelected : "Select archetype",
        }
    },
    created() {
        console.log(this.archetypeSelected)
    },
}
</script>
<style lang="scss" scoped>
    
</style>