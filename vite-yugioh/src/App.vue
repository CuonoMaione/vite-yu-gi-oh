<template>
  
  <AppHeader/>
  <AppMain/>

</template>
<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';


export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
  },

}

</script>
<style lang="scss">
  @import'../src/styles/general.scss' ;
  @import "bootstrap/scss/bootstrap";

</style>
