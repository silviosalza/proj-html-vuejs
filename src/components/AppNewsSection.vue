<script>
import AppCard from './AppCard.vue'
import AppCardSmall from './AppCardSmall.vue';
export default{
    name: "AppNewsSection",  
    components: {
        AppCard,
        AppCardSmall

    },
    data(){
      return{
        news: [
          {
            title: "Smartphone and cars, how to optimize the features",
            subtitle: "October 11th,2015 | 2 Comments",
            paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
            img: "../src/assets/img/post_feat_img_25-320x202.jpg",
            guide: false
          },
          {
            title: "How AI are revolutionizing photography",
            subtitle: "October 11th,2015 | Comments Off",
            paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
            img: "../src/assets/img/post_feat_img_24-320x202.jpg",
            guide: false
          },
          {
            title: "Are Smartwatches just a market bubble?",
            subtitle: "October 11th,2015 | Comments Off",
            paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
            img: "../src/assets/img/post_feat_img_23-320x202.jpg",
            guide: false
          },
          {
            title: "Guide to the best E-Books on the market",
            subtitle: "October 11th,2015 | Comments Off",
            paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
            img: "../src/assets/img/post_feat_img_22-320x202.jpg",
            guide: true
          },
          {
            title: "Guide to the best telephoto lenses for long shots",
            subtitle: "October 11th,2015 | Comments Off",
            paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
            img: "../src/assets/img/post_feat_img_21-320x202.jpg",
            guide: true
          },
          {
            title: "Guide to the most aesthetically elegant laptops",
            subtitle: "October 11th,2015 | Comments Off",
            paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ad voluptatem, repudiandae hic modi quaerat facilis nemo reiciendis incidunt, debitis quam saepe cum possimus aut maiores molestias illum sapiente unde.",
            img: "../src/assets/img/post_feat_img_20-320x202.jpg",
            guide: true
          }, 
        ],
      }
    },
}


</script>


<template>
    <div class="container">
        <section class="title_section d-flex flex-column align-items-center gap-3">
          <h6>AVADA TECH FORUM</h6>
          <h2>All the latest news</h2>
          <div class="pseudoelem_orange"></div>
        </section>
        <div class="row d-flex justify-content-center">
          <template v-for="(news,index) in news" :key="index">
            <AppCard v-if="news.guide === false" :title = "news.title" :subtitle="news.subtitle" :paragraph="news.paragraph" :img="news.img" />
          </template>
        </div>
        <div class="featured_article">
            <h6>FEATURED ARTICLE</h6>
            <h2>
              Apple presents the new generation of Smartwatches
            </h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ea est a blanditiis, quos ex consequatur consectetur pariatur sint voluptate placeat molestias in odit perspiciatis ipsa. Aspernatur illo itaque quod veniam?</p>
            <button type="button" class="btn btn-dark"><span>READ MORE</span><i class="fa-solid fa-chevron-right"></i></button>
        </div>
        <div class="row d-flex justify-content-center">
            <template v-for="(news,index) in news" :key="index">
              <AppCard v-if="news.guide === true" :title = "news.title" :subtitle="news.subtitle" :paragraph="news.paragraph" :img="news.img"/>
            </template>
        </div>
        <div class="row">
          <div class="col-8 review_article">
            <h6>REVIEWED PRODUCT</h6>
            <h2>Garmin Forerunner smartwatch review</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ea est a blanditiis, quos ex consequatur consectetur pariatur sint voluptate placeat molestias in odit perspiciatis ipsa. Aspernatur illo itaque quod veniam?</p>
            <button type="button" class="btn btn-dark"><span>READ MORE</span><i class="fa-solid fa-chevron-right"></i></button>
          </div>
          <div class="col-4">
            <h3>News & Guides</h3>
            <div class="pseudoelem_orange"></div>
            <template v-for="(news,index) in news" :key="index">
              <AppCardSmall v-if="index <= 2" :title = "news.title" :subtitle="news.subtitle" :img="news.img"/>
            </template>
          </div>
        </div>
    </div>
    <div class="section_footer d-flex justify-content-center align-items-center">
      <button type="button" class="btn btn-dark"><span>READ OUR BLOG</span><i class="fa-solid fa-arrow-right"></i></button>
    </div>


</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.row{
  padding: 0.2rem;
}
.featured_article{
    background-image: url(../assets/img/featured_article_1_bg.jpg);
    background-size: cover;
    margin: 3rem 0;
    padding: 12rem 5rem 8rem 5rem;
    color: $white_text;
    h2{
      padding: 1rem 0;
    }
    p{
      padding-bottom: 1rem;
    }
}
.review_article.col-8{
  background-image: url(../assets/img/featured_article_2_bg.jpg);
  color: $white_text;
  background-size: cover;
  margin: 3rem 0;
  padding: 12rem 5rem 8rem 5rem;
  .btn{
    border: $grey_text 1px solid;
  }

}
.col-4{
  padding: 3rem 0rem 0 2rem;
  .pseudoelem_orange{
    margin: 2rem 0;
  }
}

</style>