<script>
import { store } from '../data/store';
export default {
    name: 'CharachterList',
    data(){
        return{
            store
        }
    }
}
</script>

<template>
  <ul>
    <li v-for="character in store.charactersList" :key="character.char_id">
    {{character.name}}
    </li>
  </ul>
</template>


<style lang="scss" scoped>

</style>