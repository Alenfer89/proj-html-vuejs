<template>
    <section id='jumbotron' class="container">
        <div class="row">
            <div class="col-4 d-flex flex-column justify-content-center me-auto">
                <h1 class="text-capitalize ax-bold">businness planning</h1>
                <h1 class="text-capitalize ms-1">digital tecnology</h1>
                <h1 class="text-capitalize ms-1 mb-4 ax-bold">modern solution !</h1>
                <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint eaque velit ut atque modi veniam officiis ullam incidunt quaerat eligendi.</p>
                <div>
                    <button class="text-capitalize me-3">try it now</button>
                    <button class="text-capitalize"> explore more</button>
                </div>
            </div>
            <div class="col-7">
                <img class="img-fluid" src="../../assets/images/header.png" alt="Work-Station in office enviroment">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'IndexJumbotron'
}
</script>

<style lang='scss' scoped>
@import '../../assets/styles/style.scss';

section#jumbotron{
    color: white;
    p{
        color: $buttonPrimaryLight;
    }
    button{
        @include betterButton($secondaryLightColor);
        @include bgGradientLeftToRight ($buttonPrimaryLight, $buttonPrimary);
        &:hover{
            @include bgGradientLeftToRight ($secondaryColor, $secondaryLightColor)
        }
        &:first-child{
            @include betterButton($buttonPrimaryLight);
            @include bgGradientLeftToRight ($secondaryColor, $secondaryLightColor);
            &:hover{
                @include bgGradientLeftToRight ($buttonPrimaryLight, $buttonPrimary);
            }
        }
    }
}
</style>