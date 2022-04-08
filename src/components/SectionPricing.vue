<template>
    <section id="pricing" class="pt-5">
        <div class="ax-bg-placeholder position-relative">
            <div class="container">
                <div class="row py-5">
                    <div class="col-6 me-auto ms-auto text-center">
                        <p class="text-capitalize">price list</p>
                        <h2 class="text-capitalize mb-3 text-white"><span class="ax-bold">our</span> pricing</h2>
                        <p class="text-white">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus quis natus eum architecto soluta quisquam consequuntur, reiciendis minima laboriosam atque omnis explicabo. Voluptate adipisci omnis quidem aliquid modi id pariatur?</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="container ax-card-container">
            <div class="row">
                <div class="col-12 d-flex justify-content-between">
                    <PriceTag v-for='(el, index) in 3' :key='index'/>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import PriceTag from './PriceTagCard.vue';

export default {
    name: 'SectionPricing',
    components:{
        PriceTag,
    }
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';

section#pricing{
    

    div.ax-bg-placeholder{
        height: 600px;
        @include bgGradientTopToBottom ($primaryLightColor , $primaryColor);

        p:first-child{
            color: $secondaryLightColor;
        }
    }
    
    div.ax-card-container{
        position: relative;
        height: 600px;
        background-color: rgb(177, 133, 133);
        width: 100%;
        bottom: 300px;
        z-index: 1;
    }
    
}
</style>