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

                    <PriceTag
                    v-for='(offer, index) in offersList'
                    :key='index'
                    :tag='offer'
                    :index='index'/>
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
    },
    data: function(){
        return{
            offersList:[
                {
                    name: 'designing',
                    type: 'process',
                    price: 40
                },
                {
                    name: 'developing',
                    type: 'product',
                    price: 80
                },
                {
                    name: 'supporting',
                    type: 'clients',
                    price: 60
                }
            ]
        }
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
        margin-bottom: -200px;
        width: 100%;
        bottom: 300px;
        left: 0;
        z-index: 1;

        div.ax-price-tag:nth-child(even){
            @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor);
            color: white;
        }
    }
}
</style>