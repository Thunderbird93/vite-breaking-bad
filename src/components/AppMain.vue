<script>
import axios from "axios";
import AppCard from "./AppCard.vue";
import {store} from "../data/store";

    export default {
        name: 'AppMain',
        components: {
            AppCard,
        },
        data(){
            return{
                store,
            }
        },
        methods: {
            getData(){
                .get(store.apiUrl)
                .then((result) => {
                    store.inData = result.data;
                })
                .catch((error)=>{
                    console.log("error");
                });
            }
        }
    }
</script>



<template>
    <div class="container">
        <div
        class="col-4"
        v-for="(character, index) in store.inData"
        :key="index">
        <AppCard :chInfo="character" />
        </div>
        <div>
            <p>Hi!</p>
        </div>
    </div>
</template>


<style lang="scss">
    body{
        background-color: green;
        .container{
            height: 100vh;
        }
    }
</style>
