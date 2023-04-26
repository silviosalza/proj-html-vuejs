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
          title: "Home",
          subtitle: "lorem ipsum",
          paragraph: "lorem ipsum",
          img: "../src/assets/img/post_feat_img_25-320x202.jpg"
        },
        {
          title: "Home",
          subtitle: "",
          paragraph: "",
          img: "../src/assets/img/post_feat_img_24-320x202.jpg"
        },
        {
          title: "Home",
          subtitle: "",
          paragraph: "",
          img: "../src/assets/img/post_feat_img_23-320x202.jpg"
        },
        
      ],
      guides: [
      {
          title: "Home",
          subtitle: "",
          paragraph: "",
          img: ""
        },
        {
          title: "Home",
          subtitle: "",
          paragraph: "",
          img: ""
        },
        {
          title: "Home",
          subtitle: "",
          paragraph: "",
          img: ""
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

    </div>


</template>

<style scoped lang="scss">


</style>