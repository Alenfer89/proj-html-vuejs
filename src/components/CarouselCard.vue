<template>
    <div class="ax-carousel-element">
        <div class="img-wrapper">
            <img :src="require(`../assets/images/${thumb}`)" :alt="name">
        </div>
        <div class="d-flex justify-content-between align-items-center">
            <h6 class="ax-bold"> {{ name }} </h6>
            <p> {{ category }} </p>
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
    width: calc(100% - 5rem) / 3;
    border-radius: 2rem;

    div.img-wrapper{
        border-radius: 2rem;
        width: 100%;
        img{
            width: 100%;
        }
    }
}
</style>