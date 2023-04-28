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
        <div class="header d-flex justify-content-between align-items-center">
            <div class="logo">
                <img src="../assets/img/logo.png" alt="">
            </div>
            <div class="nav">
                <AppNavbar v-for="(menu,index) in menu" :key="index" :title = "menu.title" :link="menu.link"/> 
                <button type="button" class="btn btn-dark">JOIN US</button>
                <span class="d-flex align-items-center">
                  <a href=""><i class="fa-solid fa-magnifying-glass mx-3"></i></a> 
                  <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Search">
                </span> 
       
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


     .header{
         height: 100%;
         padding: 0 10rem;
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
.fa-magnifying-glass{
  font-size: 1.5rem;
}
a:hover i{
  color: black;
}
.form-control{
  border-radius: 0;
}



</style>