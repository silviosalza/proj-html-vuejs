<script>
import AppHeader from "./components/AppHeader.vue"
import AppJumbotron from "./components/AppJumbotron.vue";
export default{
  components: {
    AppHeader,
    AppJumbotron
},
  data(){
    return{
      
    }
  }
}
</script>

<template>
  <AppHeader/>
  <AppJumbotron/>
  
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/utilities/variables" as *;

</style>
