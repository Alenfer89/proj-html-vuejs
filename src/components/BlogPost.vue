<template>
    <div class="ax-blog-post d-flex justify-content-between rounded-3 text-white"
    :class="(focus === true) ? 'col-6 ' : 'col-3' ">
        <div>
            <p> {{ focus }} </p>
            <p> {{ date }} / {{ author }} </p>
            <h3> {{ title }} </h3>
            <p> {{ article }} </p>
        </div>
        <button>Read More</button>
    </div>
</template>

<script>
export default {
    name: 'BlogPost',
    props:{
        title: String,
        article: String,
        author: String,
        date: String,
        focus: Boolean
    }
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';

div.ax-blog-post{
    height: 400px;
    background-color: rgb(22, 22, 115);
}
</style>