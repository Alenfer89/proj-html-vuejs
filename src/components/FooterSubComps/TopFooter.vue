<template>
    <section class="position-relative">
        <div id="footer-banner" class="container">
            <div class="row">
                <div class="col">
                    <h1>subscribe</h1>
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

div#footer-banner{
    top: 0;
    left: 0;
    transform: translateY(-50%);
    @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor)
}

</style>