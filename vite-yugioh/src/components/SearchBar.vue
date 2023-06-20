<template>
    <div class="container-lg">
        <div class="row">
            <div class="col-5">
                <div class="input-group mb-3">
                    <select class="form-select" id="inputGroupSelect01" v-model="archetypeSelected">
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
            archetypeList : ['All','Alien','Noble Kinght','A.I.','Ignister'],
            archetypeSelected : "All",
        }
    },
    created() {
        console.log(this.archetypeSelected)
    },
}
</script>
<style lang="scss" scoped>
    
</style>