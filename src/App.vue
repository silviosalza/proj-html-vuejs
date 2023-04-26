<script>
import AppHeader from "./components/AppHeader.vue";
import AppNavbar from "./components/AppNavbar.vue";
import AppJumbotron from "./components/AppJumbotron.vue";
import AppNewsSection from "./components/AppNewsSection.vue";
export default{
  components: {
    AppHeader,
    AppNavbar,
    AppJumbotron,
    AppNewsSection
},
}
</script>

<template>
  <AppHeader/>
  <AppJumbotron/>
  <AppNewsSection/>
  
  
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/utilities/variables" as *;

body{
  font-family: $main-font;
}

</style>
