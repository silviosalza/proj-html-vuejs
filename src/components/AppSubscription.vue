<script>
export default {
    name: "AppSubscription",
   
}

</script>

<template>
    <div class="join_section">
        <div class="container">
            <h2 class="text-center">Hey! Join to our<br>Community</h2>
            <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate laudantium a, velit odit, consequuntur nisi soluta similique sequi nam distinctio ipsam rem? Repellat est soluta enim provident reprehenderit sunt suscipit!</p>
            <div class="d-flex justify-content-center" >
                <button type="button" class="btn btnBlu"><span>SIGN UP</span><i class="fa-solid fa-chevron-right"></i></button>
            </div>
        </div>
    </div>
    <div class="subscribe_section">
        <div class="container">
            <h4 class="text-center pb-4">Subscribe to our Newsletter</h4>
            <div class="input-group mb-3">
                <input type="text" class="form-control" placeholder="Insert your email" aria-label="Recipient's username" aria-describedby="basic-addon2">
                <button type="button" class="btn btn-dark px-5"><span>SEND</span></button>
            </div>
        </div>
    </div>


</template>

<style scoped lang="scss">
@use "../styles/general.scss" as *;
@use "../styles/utilities/variables" as *;
.join_section{
    background-image: url(../assets/img/join_now_cta_bg.jpg);
    color: $white_text;
    h2{
        font-size: 3rem;
    }
}
.container{
    padding: 7rem 15rem;  
}
.subscribe_section{
    background-color: #f2f2f2;
}
.form-control{
    margin-right: 1rem;
    border-radius: 0;
}




</style>