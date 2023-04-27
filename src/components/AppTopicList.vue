<script>
export default{
    name: "AppTopicList",
    props: {
        title: String,
        post: String, 
        likes: String   
    }
}

</script>

<template>
    <ul>
        <li>
            <i class="fa-solid fa-chevron-right"></i><a href="">{{ title }}</a>
            <a href="">{{ post }}</a>
            <hr>
        </li>
    </ul>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

ul{
    list-style:none;
    li a{
        text-decoration: none;
        color: inherit;
    }
   li{
    font-size: 0.8rem;
    .fa-chevron-right{
        padding-right: 0.5rem;
    }
   }
    
}

</style>

