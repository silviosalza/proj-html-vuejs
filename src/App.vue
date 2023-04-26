<script>
import AppHeader from "./components/AppHeader.vue";
import AppNavbar from "./components/AppNavbar.vue";
import AppJumbotron from "./components/AppJumbotron.vue";
export default{
  components: {
    AppHeader,
    AppNavbar,
},
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
