<template>
    <div class="col text-center">
        <div class="ax-image-wrapper mb-5">
            <img class="img-fluid" :src="require(`../assets/images/${image}`)" :alt="name +' profile pic'">
        </div>
        <div class="mb-5">
            <p class="mb-4">
                <i class="fa-solid fa-star"
                v-for='(element, index) in rating'
                :key="'full-star ' + index">
                </i>
                <i class="fa-regular fa-star"
                v-for='(element, index) in 5-rating'
                :key="'empty-star ' + index">
                </i>
            </p>
            <p> {{ text }} </p>
        </div>
        <div>
            <h6 class="ax-bold"> {{ name }} </h6>
            <p> {{ role }} </p>
        </div>
    </div>
</template>

<script>


export default {
    name: 'ReviewCard',
    props:{
        name:String,
        role:String,
        text:String,
        image:String,
        rating:Number
    }
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';
div.ax-image-wrapper{
    width: 110px;
    height: 110px;
    margin: 0 auto;
    border-radius: 50%;
    border: 4px solid $secondaryColor;
}
i.fa-solid.fa-star{
    @include bgGradientTopToBottom ($secondaryColor , $secondaryLightColor);
    background-clip: text;
    color: transparent;
    //-webkit-text-fill-color: transparent;
}
i.fa-regular.fa-star{
    @include bgGradientTopToBottom ($secondaryColor , $secondaryLightColor);
    background-clip: text;
    color: transparent;
    //-webkit-text-fill-color: transparent;
}

</style>