<template>
    <section id='businness' class="py-5">
        <div class="container">
            <div class="row py-5 justify-content-center align-items-center">
                <div class="col-5 me-auto p-5">
                    <div class="ax-image-wrapper position-relative">
                        
                        <img class="img-fluid position-absolute ax-on-bg-image" src="../assets/images/nemoodar.png" alt="Work-Station in office enviroment">
                        <img class="img-fluid ax-on-top-image" src="../assets/images/men-data.png" alt="Work-Station in office enviroment">
                    </div>
                </div>
                <div class="col-5 p-5 d-flex flex-column justify-content-between">
                    <h6 class="text-capitalize mb-5">start your project</h6>
                    <h1 class="text-capitalize">
                        <span class="ax-bold">grow your businness</span>
                        <br>
                        with our strategy
                    </h1>
                    <p class="my-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia nam laborum placeat animi quisquam possimus voluptates numquam natus quia ullam delectus quas ducimus pariatur earum optio culpa, amet iste! Nihil.</p>
                    <div>
                        <button class="text-capitalize me-3">try it now</button>
                        <button class="text-capitalize"> explore more</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionBusinness',
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';

section#businness{
    color: white;
    @include bgGradientTopToBottom($primaryLightColor, $primaryColor);

    img.ax-on-bg-image{
        top: -2.5rem;
        left: -3rem;
        z-index: 0;
    }
    img.ax-on-top-image{
        position: relative;
        z-index: 1;
    }

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