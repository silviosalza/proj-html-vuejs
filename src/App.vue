<script>
import AppHeader from "./components/AppHeader.vue";
import AppNavbar from "./components/AppNavbar.vue";
import AppJumbotron from "./components/AppJumbotron.vue";
export default{
  components: {
    AppHeader,
    AppNavbar,
    AppJumbotron
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

body{
  font-family: $main-font;
}

</style>
