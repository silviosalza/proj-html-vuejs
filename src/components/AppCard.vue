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
    <div class="card col-4" style="width: 18rem;">
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

</style>