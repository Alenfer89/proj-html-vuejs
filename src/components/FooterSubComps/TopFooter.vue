<template>
    <section class="position-relative mt-5">
        <div id="footer-tag" class="position-relative">
            <div class="container">
                <div class="row">
                    <div class="col d-flex justify-content-between align-items-center p-5 w-50">
                        <div>
                            <h1 class="text-capitalize ax-bold">we offer awesome services</h1>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                        <div class="ax-input-wrapper p-2 ms-5 text-end bg-white d-flex">
                            <input type="text" class="flex-grow-1" placeholder="Enter Your Email Address">
                            <button class="" type="button">Subscribe</button>
                        </div>
                        
                    </div>
                </div>
            </div>
        </div>
        
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1>links</h1>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name:'TopFooter'
}
</script>

<style lang='scss' scoped>
@import '../../assets/styles/style.scss';

div#footer-tag{
    top: 0;
    left: 0;
    transform: translateY(-50%);
    div.col{
        @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor);
        height: 12rem;
    }
    div.ax-input-wrapper{
        border-radius: 50rem;
        width: 40%;
    }
    input{
        border: none;
        border-radius: 50rem;
        &:focus{
            outline: none;
        }
    }
    button{
        @include betterButton($secondaryLightColor);
        @include bgGradientLeftToRight ($buttonPrimaryLight , $buttonPrimary);
        &:hover{
            @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor);
        }
    }
}

</style>