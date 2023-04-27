<script>
import AppForumCard from './AppForumCard.vue';

export default {
    name: "AppForums",
    components: {
        AppForumCard
    },
    data(){
      return{
        forum: [
            {
                title: "News & Community",
                icon: "fa-solid fa-file"
            },
            {
                title: "Apple Forum",
                icon: "fa-brands fa-apple"
            },
            {
                title: "Microsoft Forum",
                icon: "fa-brands fa-windows"
            },
            {
                title: "Android Forum",
                icon: "fa-brands fa-android"
            },
            {
                title: "General Discussion",
                icon: "fa-solid fa-mug-saucer"
            },
            {
                title: "Apps & Software",
                icon: "fa-solid fa-cubes"
            },
            {
                title: "Gadgets & Stuff",
                icon: "fa-solid fa-laptop"
            },
            {
                title: "Tutorials & Guides",
                icon: "fa-solid fa-wrench"
            },
        ],
      }
    },
}

</script>

<template>
    <div class="forum-section">
        <div class="container pb-4">
            <section class="title_section d-flex flex-column align-items-center gap-3">
              <h6>AVADA TECH FORUM</h6>
              <h2>Forum Sections</h2>
              <div class="pseudoelem_orange"></div>
            </section>
            <div class="row d-flex justify-content-center">
                <template v-for="(forum,index) in forum" :key="index">
                <AppForumCard :title = "forum.title" :icon="forum.icon"/>
              </template>
            </div>
        </div>
    </div>
    <div class="section_footer d-flex justify-content-center align-items-center">
        <button type="button" class="btn btn-dark"><span>GO TO OUR FORUM</span><i class="fa-solid fa-arrow-right"></i></button>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.forum-section{
    background-color: #f2f2f2;
}
.row{
    padding: 0;
    margin: 0;
    width: 100%;
}



</style>