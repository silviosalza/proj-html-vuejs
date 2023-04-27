<script>
export default {
    name: "AppJumbotron",
}

</script>

<template>
    <section class="jumbotron_top d-flex align-items-center">
        <div class="container">
            <h1>Tech Forum!</h1>
            <p>Discuss al the latest technology news and trends</p>
            <button type="button" class="btn"><span>GET AVADA NOW!</span><i class="fa-solid fa-chevron-right"></i></button>
        </div>
    </section>
    <div class="jumbotron_bottom">
        <div class="container text-center">
            <div class="forum_info">
                <h6>AVADA FORUM IS THE PLACE TO BE</h6>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic assumenda sapiente corrupti ipsum dolore, tenetur pariatur mollitia consectetur fuga error optio. Deleniti fugit earum laudantium dolor nemo ab dicta natus!Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic assumenda sapiente corrupti ipsum dolore, tenetur pariatur mollitia consectetur fuga error optio. Deleniti fugit earum laudantium dolor nemo ab dicta natus!</p>
            </div>
        </div>
    </div>


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
    .btn{
        color: $white_text;
        background-color: $header_color;
        display: flex;
        align-items: center;
        gap: 0.5rem;
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

</style>