<template>
    <section class="position-relative mt-5">
        <div id="footer-tag" class="position-relative">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <h1>subscribe</h1>
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
}

</style>