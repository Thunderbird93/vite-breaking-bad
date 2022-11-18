<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue';

export default {
  name: 'App',
  components:{
    AppHeader,
    AppFooter,
    AppMain
  },
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
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>


<style lang="scss" scoped>
  @use './styles/general.scss'
</style>