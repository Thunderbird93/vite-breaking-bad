<script>
import { store } from '../data/store';
import CharacterCard from './CharacterCard.vue';
export default {
    name: 'CharachterList',
    components:{
        CharacterCard
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>
    <CharacterCard v-for="character in store.charactersList" :key="character.char_id"/>
  <ul>
    <li v-for="character in store.charactersList" :key="character.char_id">
    {{character.name}}
    </li>
  </ul>
</template>


<style lang="scss" scoped>

</style>