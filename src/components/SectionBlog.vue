<template>
    <section id="blog">
        <div class="container">
            <div class="row py-5">
                <div class="col-6 me-auto ms-auto text-center">
                    <p class="text-capitalize">blog</p>
                    <h2 class="text-capitalize mb-3"><span class="ax-bold">latest</span> post</h2>
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus quis natus eum architecto soluta quisquam consequuntur, reiciendis minima laboriosam atque omnis explicabo.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionBlog',
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