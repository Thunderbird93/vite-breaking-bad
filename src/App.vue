<script>
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
  data(){
    return{
    }
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