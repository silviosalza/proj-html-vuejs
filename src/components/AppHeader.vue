<script>
import AppNavbar from './AppNavbar.vue';

export default{
    name: "AppHeader",  
    components: {
        AppNavbar,
    },
    data(){
    return{
      menu: [
        {
          title: "Home",
          link: ""
        },
        {
          title: "Apple",
          link:""
        },
        {
          title: "Microsoft",
          link:""
        },
        {
          title: "Android",
          link:""
        },
        {
          title: "Forums",
          link:""
        },
        {
          title: "Contact Us",
          link:""
        },
      ]
      
    }
  }
}
</script>

<template>
    <header id="header">
        <div class="container d-flex justify-content-between">
            <div class="logo">
                <img src="../assets/img/logo.png" alt="">
            </div>
            <div class="nav">
                <AppNavbar v-for="(menu,index) in menu" :key="index" :title = "menu.title" :link="menu.link"/> 
                <button type="button" class="btn btn-dark">JOIN US</button>
                <span><i class="fa-solid fa-magnifying-glass"></i></span>        
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

header{
    height: 100px;
    background-color: $header_color;
    color: $white_text;
    font-weight: 700;


    .container{
        height: 100%;
    }
    .logo{
        height: 100%;
        display: flex;
        align-items: center;
    }
    .nav{
        height: 100%;
        display: flex;
        align-items: center;
        gap: 2rem;
    }
    ul{
        margin: 0;
        padding: 0;
    }
}



</style>