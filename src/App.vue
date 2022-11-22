<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';

export default {
  name: 'App',
  components:{
    AppHeader,
    AppMain,
    AppFooter,
  },
  /*
  methods:{
    getCharacters(){
      axios.get('https://www.breakingbadapi.com/api/characters')
    .then(result =>{
      console.log(result.data)
    })
    .catch.log(error =>{
      console.log(errore)
    })
    }
  },

  mounted(){
    this.getCharacters();
  }
*/  
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>


<style lang="scss" scoped>

</style>