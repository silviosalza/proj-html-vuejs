<script>
export default {
    name: "AppCard",
    props: {
        title: String,
        subtitle: String,
        paragraph: String,
        img: String, 
         
    }
}

</script>

<template>
    <div class="card ms_card col-4">
        <img :src="img" class="card-img-top" alt="...">
        <div class="card-body">
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
    padding: 0.5rem;
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

</style>