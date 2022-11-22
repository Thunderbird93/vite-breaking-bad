<script>
import axios from 'axios'
import AppHeader from "./components/AppHeader.vue"
import AppSearch from "./components/AppSearch.vue"
import CharacterList from "./components/CharacterList.vue"

export default {
  name: "App",
  components:{
    AppHeader,
    AppSearch,
    CharacterList
  },
  methods:{
    getCharacters(){
      axios.get('https://www.breakingbadapi.com/api/characters')
      .then(result => {
      console.log(result.data)
    })
    .catch(error => {
      console.log(error)
    })
    }
  },

  mounted(){
    this.getCharacters();
  }
}
</script>

<template>
  <AppHeader title="Breaking Bad Api"/>
  <main>
    <AppSearch />
    <CharacterList />
  </main>
</template>

<style lang="scss" scoped>

</style>