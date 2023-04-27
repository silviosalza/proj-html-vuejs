<script>
import AppTopicList from "./AppTopicList.vue"

export default{
    name: "AppFooter",  
    components: {
        AppTopicList,

    },
    data(){
      return{
        topics: [
          {
            title: "Official Topic Cinema & TV Series",
            post: "Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt",
            likes: "",
          },
          {
            title: "Official Topic Smarthphone",
            post: "Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt",
            likes: "",
          },
          {
            title: "Official Topic Hardware PC",
            post: "Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt",
            likes: "",
          },
          {
            title: "Official Topic Console & Videogames",
            post: "Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt",
            likes: "",
          },
          
        ],
      }
    },
}

</script>

<template>
    <section class="footer_top">
        <div class="container">
            <div class="row">
                <div class="col-3">
                    <h5>AVADA TECH FORUM</h5>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum quas ea, animi laborum nisi possimus nemo corporis! Tenetur natus, ipsa labore repudiandae sint quisquam tempore alias hic beatae, eaque quaerat!</p>
                </div>
                <div class="col-3">
                    <h5>POPULAR TOPICS</h5>
                    <AppTopicList v-for="(element,index) in topics" :key="index" :title = "element.title"/>
                </div>
                <div class="col-3">
                    <h5>RECENT TOPICS</h5>
                    <AppTopicList v-for="(element,index) in topics" :key="index" :title = "element.title"/>
                </div>
                <div class="col-3">
                    <h5>LATER REPLIES</h5>
                    <AppTopicList v-for="(element,index) in topics" :key="index" :post = "element.post.slice(0 , 30)"/>
                </div>
            </div>
        </div>
    </section>
    <div class="container footer_bottom py-3 d-flex justify-content-between align-items-center">
        <div class="footer_info">
            <p>Copyright 2012 - 2020 | Avada Theme by <strong>Theme Fusion</strong> | All Rights Reserved | Powered by <strong>WordPress</strong></p>
        </div>
        <div class="social_link d-flex">
            <a href=""><div class="circle fb px-3 d-flex justify-content-center align-items-center"><i class="fa-brands fa-facebook-f"></i></div></a>
            <a href=""><div class="circle tw px-3 d-flex justify-content-center align-items-center"><i class="fa-brands fa-twitter"></i></div></a>
            <a href=""><div class="circle in px-3 d-flex justify-content-center align-items-center"><i class="fa-brands fa-instagram"></i></div></a>
            <a href=""><div class="circle yt px-3 d-flex justify-content-center align-items-center"><i class="fa-brands fa-youtube"></i></div></a>
        </div>
    </div>

</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.footer_top{
    padding: 5rem 10rem;
    border-bottom: 3px solid #f2f2f2;
    h5{
        padding-bottom: 2rem;
    }
    ul{
        padding: 0;
    }
}
.footer_bottom{
    padding: 0rem 7rem;
}
a{
    text-decoration: none;
    color: inherit;
    padding: 0 0.3rem;
}
.footer_info{
    font-size: 0.8rem;
    p{
        margin-bottom: 0;
    }
}
.circle{
    height: 50px;
    width: 50px;
    border-radius: 50%;
    color: white;
    font-size: 1.5rem;
    &.yt{
        background-color: rgb(229, 45, 45);
    }
    &.fb{
        background-color: rgb(41, 150, 218);
    }
    &.tw{
        background-color: lightskyblue;
    }
    &.in{
        background-color: rgb(109, 20, 169);
    }
}


</style>