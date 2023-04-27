<script>
export default {
    name: "AppForumCard",
    props: {
        title: String,
        icon: String,    
    }
}
</script>

<template>
    <div class="card col-2">
        <div class="circle d-flex justify-content-center align-items-center">
            <i :class="icon"></i>
        </div>
        <h5>{{ title }}</h5>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.card.col-2{
    margin: 2rem;
    border: 0;
    border-top: 3px solid $header_color;
    border-radius: 0;
    padding: 3rem 0;
    display: flex;
    justify-content: center;
    align-items: center;

}
.circle{
    height: 6rem;
    width: 6rem;
    background-color: $orange_detail; 
    border-radius: 50%;    
    i{
        font-size: 3rem;
        color: $white_text;
    }
}

</style>