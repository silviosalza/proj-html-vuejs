<script>
export default {
    name: "AppCard",
    props: {
        title: String,
        subtitle: String,
        paragraph: String,
        img: String, 
        imgSmall: String,
         
    }
}

</script>

<template>
    <div class="card ms_card col-4">
        <img :src="img" class="card-img-top" alt="...">
        <div class="card-body px-2">
            <h3>{{ title }}</h3>
            <h4>{{ subtitle }}</h4>
            <p>{{ paragraph }}</p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

.card.ms_card{
    border: 0;
    padding: .2rem;
    cursor: pointer;
    .card-img-top{
        border-radius: 0;
    }
    .card-body{
        padding: 1rem 0 0 0;
        h3{
            font-size: 1.1rem;
        }
        h4{
            font-size: 0.7rem;
        }
        p{
            font-size:0.9rem ;
            margin-bottom: 0;
        }
    }
}

.card:hover {
    transform: scale(105%);
    transition-duration:.5s;
    z-index: 999 ;
}
.card:hover .card-body{
    background-color: #27aabe10;
}

</style>