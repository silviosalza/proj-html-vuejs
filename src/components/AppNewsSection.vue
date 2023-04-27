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
        }
        
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
        <section class="news d-flex flex-column align-items-center gap-3">
          <h6>AVADA TECH FORUM</h6>
          <h2>All the latest news</h2>
          <div class="pseudoelem_orange"></div>
        </section>
        <div class="row d-flex justify-content-center">
            <AppCard v-for="(news,index) in news" :key="index" :title = "news.title" :subtitle="news.subtitle" :paragraph="news.paragraph" :img="news.img" />
        </div>
        <div class="featured_article">
            <h6>FEATURED ARTICLE</h6>
            <h2>
                Apple presenta la nuova generazione di Smartwatch
            </h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ea est a blanditiis, quos ex consequatur consectetur pariatur sint voluptate placeat molestias in odit perspiciatis ipsa. Aspernatur illo itaque quod veniam?</p>
            <button type="button" class="btn btn-dark"><span>READ MORE</span><i class="fa-solid fa-chevron-right"></i></button>
        </div>
        <div class="row d-flex justify-content-center">
            <AppCard v-for="(guide,index) in guides" :key="index" :title = "guide.title" :subtitle="guide.subtitle" :paragraph="guide.paragraph" :img="guide.img" />
        </div>
    

    </div>


</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.news{
  padding: 4rem 0;
  .pseudoelem_orange{
    width: 100px;
    background-color: rgb(255, 188, 63);
    height: 2px;
    
  }
  
  h6{
    color: $grey_text;
  }
}
.row{
  margin: 0;

}
.featured_article{
    background-image: url(../assets/img/featured_article_1_bg.jpg);
    background-size: cover;
    margin: 3rem 0.5rem;
    padding: 12rem 5rem 8rem 5rem;
    color: $white_text;
    h2{
      padding: 1rem 0;
    }
    p{
      padding-bottom: 1rem;
    }

    .btn{
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }
}


</style>