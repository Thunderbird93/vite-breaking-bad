<script>
import {store} from '../data/store'

export default {
    name: 'AppSearch',
    data(){
        return{
            store
        }
    }
}
</script>

<template>
  <select @change="$emit('search')" v-model="store.thatSeries" class="form-select">
    <option value="">Select category</option>
    <option value="Breaking Bad">Breaking Bad</option>
    <option value="Better Call Saul">Better Call Saul</option>
  </select>
</template>

<style lang="scss" scoped>

</style>