<script>
import AppHeader from "./components/AppHeader.vue";
import AppJumbotron from "./components/AppJumbotron.vue";
import AppNewsSection from "./components/AppNewsSection.vue";
import AppForums from "./components/AppForums.vue";
import AppSubscription from "./components/AppSubscription.vue";
import AppFooter from "./components/AppFooter.vue";
export default{
  components: {
    AppHeader,
    AppJumbotron,
    AppNewsSection,
    AppForums,
    AppSubscription,
    AppFooter
},
}
</script>

<template>
  <AppHeader/>
  <AppJumbotron/>
  <AppNewsSection/>
  <AppForums/>
  <AppSubscription/>
  <AppFooter/>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/utilities/variables" as *;

body{
  font-family: $main-font;
}

</style>
