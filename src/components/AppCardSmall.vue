<script>
export default {
    name: "AppCardSmall",
    props: {
        title: String,
        subtitle: String,
        img: String,
    }
}

</script>

<template>
    <div class="cardSmall d-flex">
        <div class="imgSmall col-5">
            <img :src="img" alt="...">
        </div>
        <div class="card-body col-7">
            <h3>{{ title }}</h3>
            <h4>{{ subtitle }}</h4>
        </div>
    </div>
</template>
<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.cardSmall{
    padding: 1rem 0;
    img{
        width: 100%;
    }

    .card-body{
        padding-left: 1rem;
        h3{
            font-size: 1.1rem;
        }
        h4{
            font-size: 0.7rem;
        }
    }
}


</style>