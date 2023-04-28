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
                <a id="link" href="">{{ title }}</a>
                <div id="triangle-down"></div>
            </li>
        </ul>
</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;

#triangle-down {
      width: 0;
      height: 0;
      border-left: 40px solid transparent;
      border-right: 40px solid transparent;
      border-top: 50px solid $header_color;
      position: absolute;
      left: calc(50% - 40px);
      top: 100%;
      display: none;
}
ul:hover #triangle-down{
  display: block;
}
li:hover #link{
  color: black;
}


ul{
    li{
            list-style: none;
            position: relative;
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