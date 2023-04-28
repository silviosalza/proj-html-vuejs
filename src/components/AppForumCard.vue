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
        <div class="flip circle d-flex justify-content-center align-items-center">
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
    cursor: pointer;

}
.circle{
    height: 6rem;
    width: 6rem;
    background-color: $orange_detail; 
    border-radius: 50%;  
    margin-bottom: 1rem;  
    i{
        font-size: 3rem;
        color: $white_text;
    }
}

.card:hover .flip{
	backface-visibility: visible !important;
	animation: flip 2s ease 1;
}
@keyframes flip {
	0% {
		transform: perspective(400px) rotateY(0);
		animation-timing-function: ease-out;
	}
	40% {
		transform: perspective(400px) translateZ(110px) rotateY(170deg);
		animation-timing-function: ease-out;
	}
	50% {
		transform: perspective(400px) translateZ(110px) rotateY(190deg) scale(1);
		animation-timing-function: ease-in;
	}
	80% {
		transform: perspective(400px) rotateY(360deg) scale(.95);
		animation-timing-function: ease-in;
	}
	100% {
		transform: perspective(400px) scale(1);
		animation-timing-function: ease-in;
	}
}

</style>