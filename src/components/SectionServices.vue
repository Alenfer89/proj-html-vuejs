<template>
    <section id="services" class="container py-5 px-3">
        <div class="row">
            <div class="col-12 text-center">
                <p class="text-capitalize">our services</p>
                <h2 class="text-capitalize mb-3"><span class="ax-bold">what</span> we do</h2>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
            </div>
            <div class="col-12 ax-cards-wrapper">
                <Service
                v-for='(service, index) in servicesList'
                :key='index'
                :service="service" />
            </div>
            <div class="col-12 text-center">
                <button class="text-capitalize"> view all services</button>
            </div>
        </div>
    </section>
</template>

<script>
import Service from './ServiceCard.vue';
export default {
    name: 'SectionServices',
    components:{
        Service,
    },
    data: function(){
        return{
            servicesList:[
                {
                    title: 'Data Analisys',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque, enim officiis? Perferendis, laudantium magni consequuntur est dicta quas expedita dolor totam illum',
                    image: 'Group-247.png'
                },
                {
                    title: 'SEO Optimization',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque, enim officiis? Perferendis, laudantium magni consequuntur est dicta quas expedita dolor totam illum',
                    image: 'Group-538.png'
                },
                {
                    title: 'Security Data',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque, enim officiis? Perferendis, laudantium magni consequuntur est dicta quas expedita dolor totam illum',
                    image: 'Group-566.png'
                },
                {
                    title: 'Branding Strategy',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque, enim officiis? Perferendis, laudantium magni consequuntur est dicta quas expedita dolor totam illum',
                    image: 'Group-567.png'
                }
            ]
        }
    }
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';
section#services{
    p:first-child{
        color: $secondaryLightColor;
    }
    div.ax-cards-wrapper{
        padding: 10rem 0;
    }
    button{
        @include betterButton($buttonPrimaryLight);
        @include bgGradientLeftToRight ($secondaryColor, $secondaryLightColor);
        &:hover{
            @include bgGradientLeftToRight ($buttonPrimaryLight, $buttonPrimary);
        }
    }
}
</style>