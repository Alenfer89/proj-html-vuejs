<template>
    <section id="testimonial" class="py-5">
        <div class="container">
            <div class="row py-5 mb-5">
                <div class="col-6 me-auto ms-auto text-center">
                    <p class="text-capitalize">testimonial</p>
                    <h2 class="text-capitalize mb-3"><span class="ax-bold">what</span> people say</h2>
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus quis natus eum architecto soluta quisquam consequuntur, reiciendis minima laboriosam atque omnis explicabo.</p>
                </div>
            </div>
            <div class="row row-cols-3 p-4">
                <Review v-for="(review, index) in reviewsList"
                :key='index'
                :name='review.name'
                :role='review.role'
                :text='review.text'
                :image='review.image'
                :rating='review.rating'/>
            </div>
            <div class="row row-cols-5 py-5">
                <div class="col text-center py-5"
                v-for='(client, index) in clientsList'
                :key="index">
                    <img :src="require(`../assets/images/${client}`)" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Review from './ReviewCard.vue';

export default {
    name: 'SectionTestimonial',
    components:{
        Review,
    },
    data: function(){
        return{
            reviewsList:[
                {
                    name: 'Michkel Anegl',
                    role: 'Marketing Management',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, dolorum nihil nisi ipsum hic repellendus voluptatum vel nesciunt repudiandae deserunt.',
                    rating: 3,
                    image: 'philipe-cavalcante-539505-unsplash-1024x1024.png'
                },
                {
                    name: 'Michkel Anegl',
                    role: 'Marketing Management',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, dolorum nihil nisi ipsum hic repellendus voluptatum vel nesciunt repudiandae deserunt.',
                    rating: 3,
                    image: 'szabo-viktor-1266895-unsplash-1024x1024.png'
                },
                {
                    name: 'Michkel Anegl',
                    role: 'Marketing Management',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, dolorum nihil nisi ipsum hic repellendus voluptatum vel nesciunt repudiandae deserunt.',
                    rating: 3,
                    image: 'fabio-spinelli-695744-unsplash-1024x1024.png'
                }
            ],
            clientsList:[
                'client-1-1.png',
                'clienty-2.png',
                'clienty-3.png',
                'clienty-4.png',
                'client-5.png'
            ]
        }
    }
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';

section#testimonial{

    p:first-child{
        color: $secondaryLightColor;
    }
}
</style>