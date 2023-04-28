<script>
export default {
    name: "AppJumbotron",
}

</script>

<template>
    <section class="jumbotron">
        <div class="jumbotron_top d-flex align-items-center">
            <div class="container">
                <h1 class="bounce-in-right">Tech Forum!</h1>
                <p>Discuss al the latest technology news and trends</p>
                <button type="button" class="btn btnBlu"><span>GET AVADA NOW!</span><i class="fa-solid fa-chevron-right"></i></button>
            </div>
        </div>
        <div class="jumbotron_bottom">
            <div class="container text-center">
                <div class="forum_info">
                    <h6>AVADA FORUM IS THE PLACE TO BE</h6>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic assumenda sapiente corrupti ipsum dolore, tenetur pariatur mollitia consectetur fuga error optio. Deleniti fugit earum laudantium dolor nemo ab dicta natus!Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic assumenda sapiente corrupti ipsum dolore, tenetur pariatur mollitia consectetur fuga error optio. Deleniti fugit earum laudantium dolor nemo ab dicta natus!</p>
                </div>
            </div>
        </div>
    </section>


</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.jumbotron_top{
    height: 800px;
    color: $white_text;
    background-image: url(../assets/img/home_slider_bg.jpg);
    background-size:cover;
    h1{
        font-size: 8rem;
    }
    
}
.jumbotron_bottom{
    background-color: #F2F2F2;
    color: $grey_text;
    .forum_info{
        padding: 6rem 10rem;
        h6{
            font-size: 0.8rem;
            font-weight: 700;
            padding-bottom: 2rem;
        }

    }

}

.jumbotron:hover .bounce-in-right {
  animation: bounce-in-right 4s ease 1;
}
@keyframes bounce-in-right {
  0% {
    opacity: 0;
    transform: translateX(2000px);
  }
  60% {
    opacity: 1;
    transform: translateX(-30px);
  }
  80% { transform: translateX(10px); }
  100% { transform: translateX(0); }
}

</style>