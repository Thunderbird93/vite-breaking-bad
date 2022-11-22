<script>
import { store } from '../data/store';
import CharacterCard from './CharacterCard.vue';

export default {
    name: 'CharachterList',
    components:{
        CharacterCard,
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>
    <div class="pagina">
        <CharacterCard v-for="character in store.charactersList" :key="character.char_id" :character="character" />
    </div>
</template>


<style lang="scss" scoped>
    .pagina{
        display: flex;
        flex-wrap: wrap;
        margin: 0 auto;
        width: 60%;
    }
</style>