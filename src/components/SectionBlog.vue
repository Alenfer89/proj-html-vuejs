<template>
    <section id="blog" class="py-5">
        <div class="container">
            <div class="row py-5">
                <div class="col-6 me-auto ms-auto text-center">
                    <p class="text-capitalize">blog</p>
                    <h2 class="text-capitalize mb-3"><span class="ax-bold">latest</span> post</h2>
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus quis natus eum architecto soluta quisquam consequuntur, reiciendis minima laboriosam atque omnis explicabo.</p>
                </div>
            </div>
            <div class="row p-0">
                <div class="col-12 p-0 d-flex justify-content-between">
                    <BlogPost
                    v-for='(blog, index) in blogNews'
                    :key='index'
                    :title='blog.title'
                    :article='blog.text'
                    :author='blog.author'
                    :date='blog.date'
                    :focus='blog.latest'
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import BlogPost from './BlogPost.vue';

export default {
    name: 'SectionBlog',
    components:{
        BlogPost,
    },
    data: function(){
        return{
            blogNews:[
                {
                    title:'Amazon get CCI nod to acquire 49% stake in',
                    text:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga facilis...',
                    author: 'Paul',
                    date: 'April 08, 2022',
                    latest: true
                },
                {
                    title:'Clearing corporations get SEBI nod to invest in overnight funds',
                    text:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga facilis...',
                    author: 'Paul',
                    date: 'April 08, 2022',
                    latest: false
                },
                {
                    title:'Shabnam Dhillion, wife of RSSB chief Gurinder Dhillon, passes away in London',
                    text:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga facilis...',
                    author: 'Paul',
                    date: 'April 08, 2022',
                    latest: false
                }
            ]
        }
    }
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';

section#blog{

    p:first-child{
        color: $secondaryLightColor;
    }
}

</style>