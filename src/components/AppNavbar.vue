<script>

export default {
    name: "AppNavbar",
    props: {
        title: String,
        link: String   
    }
}
</script>

<template>
        <ul>
            <li>
                <a href="">{{ title }}</a>
            </li>
        </ul>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

ul{
    li{
            list-style: none;
            padding: 0;
            margin: 0;
            text-align: center;
            a{
                text-decoration: none;
                color: inherit;
            }
    }
}
</style>