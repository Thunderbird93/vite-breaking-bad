<script>

import axios from 'axios'
import {store} from './data/store'

import AppHeader from "./components/AppHeader.vue"
import AppSearch from "./components/AppSearch.vue"
import CharacterList from "./components/CharacterList.vue"

export default {
  name: "App",
  data(){
    return{
      store
    }
  },
  components:{
    AppHeader,
    AppSearch,
    CharacterList
  },
  methods:{
    getCharacters(){
      axios.get(store.apiUrl, {
        params:{
          category: store.thatSeries,
        }
      })
      .then(result => {
      console.log(result.data)
      store.charactersList = result.data
      console.log(result.data)
     })
    .catch(error => {
      console.log(error)
     })
    }
  },

  mounted(){
    this.getCharacters();
  },
}
</script>

<template>
  <AppHeader title="Breaking Bad Api"/>
  <main>
    <AppSearch @search="getCharacters()"/>
    <CharacterList />
  </main>
</template>

<style lang="scss" scoped>
 
</style>