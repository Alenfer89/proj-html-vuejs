<template>
    <div class="ax-carousel-element shadow">
        <div class="img-wrapper">
            <img :src="require(`../assets/images/${thumb}`)" :alt="name">
        </div>
        <div class="d-flex justify-content-between">
            <h6 class="ax-bold p-2"> {{ name }} </h6>
            <p class="m-0 p-2"> {{ category }} </p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CarouselCard',
    props:{
        name: String,
        category: String,
        thumb: String
    }
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';
div.ax-carousel-element{
    width: calc((100% / 5) - .5rem);
    border-radius: 2rem;
    &:hover{
        color: white;
        cursor: pointer;
        @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor);
    }

    div.img-wrapper{
        border-radius: 2rem;
        width: 100%;
        img{
            width: 100%;
            border-radius: 2rem
        }
    }
}
</style>