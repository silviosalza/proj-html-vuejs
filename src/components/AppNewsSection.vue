<script>
import AppCard from './AppCard.vue';
export default{
    name: "AppNewsSection",  
    components: {
        AppCard,
    },
    data(){
    return{
      news: [
        {
          title: "Smartphone e auto, come ottimizzare il binomio",
          subtitle: "October 11th,2015 | 2 Comments",
          paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
          img: "../src/assets/img/post_feat_img_25-320x202.jpg"
        },
        {
          title: "Come le IA stanno rivoluzionando la fotografia",
          subtitle: "October 11th,2015 | Comments Off",
          paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
          img: "../src/assets/img/post_feat_img_24-320x202.jpg"
        },
        {
          title: "Gli Smartwatch sono solo una bolla?",
          subtitle: "October 11th,2015 | Comments Off",
          paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
          img: "../src/assets/img/post_feat_img_23-320x202.jpg"
        },
        
      ],
      guides: [
      {
          title: "Guida ai migliori E-Book sul mercato",
          subtitle: "October 11th,2015 | Comments Off",
          paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
          img: "../src/assets/img/post_feat_img_22-320x202.jpg"
        },
        {
          title: "Guida ai migliori tele-obbiettivi per i campi lunghi",
          subtitle: "October 11th,2015 | Comments Off",
          paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
          img: "../src/assets/img/post_feat_img_21-320x202.jpg"
        },
        {
          title: "Guida ai laptop esteticamente più eleganti",
          subtitle: "October 11th,2015 | Comments Off",
          paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
          img: "../src/assets/img/post_feat_img_20-320x202.jpg"
        },
      ]
      
    }
  }
}


</script>


<template>
    <div class="container">
        <div class="row">
            <AppCard v-for="(news,index) in news" :key="index" :title = "news.title" :subtitle="news.subtitle" :paragraph="news.paragraph" :img="news.img" />
        </div>
        <div class="featured_article">
            <h3>
                Apple presenta la nuova generazione di Smartwatch
            </h3>

        </div>
        <div class="row">
            <AppCard v-for="(guide,index) in guides" :key="index" :title = "guide.title" :subtitle="guide.subtitle" :paragraph="guide.paragraph" :img="guide.img" />
        </div>
    

    </div>


</template>

<style scoped lang="scss">
.featured_article{
    background-image: url(../assets/img/featured_article_1_bg.jpg);
}


</style>