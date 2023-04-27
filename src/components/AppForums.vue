<script>

export default {
    name: "AppForums",
    props: {
        title: String,
        icon: String,
     
    }
}

</script>

<template>
    <div class="container">
        <section class="title_section d-flex flex-column align-items-center gap-3">
          <h6>AVADA TECH FORUM</h6>
          <h2>Forum Sections</h2>
          <div class="pseudoelem_orange"></div>
        </section>
    </div>




    <div class="section_footer d-flex justify-content-center align-items-center">
        <button type="button" class="btn btn-dark"><span>GO TO OUR FORUM</span><i class="fa-solid fa-arrow-right"></i></button>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;


</style>