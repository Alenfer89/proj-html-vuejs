<template>
    <div class="ax-blog-post p-5 d-flex justify-content-between text-white"
    :class="(focus === true) ? 'ax-main-post align-items-end' : 'ax-secondary-post flex-column' ">
        <div class="pe-3" :class="(focus===true)? 'ax-w-70' : ''">
            <p class="p-0 m-0"> {{ date }} / {{ author }} </p>
            <h5 class="ax-bold py-3"> {{ title }} </h5>
            <p class="p-0 m-0"> {{ article }} </p>
        </div>
        <div>
            <button class="d-block">Read More</button>
        </div>
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
    height: 500px;
    background-color: rgb(22, 22, 115);
    border-radius: 2rem;
    div.ax-w-70{
        width: 70%;
    }
    button{
        @include betterButton(white);
        @include bgGradientTopToBottom(white , white);
        color: black;
    }
}
div.ax-main-post{
        width: calc(50% - 1rem);
        background-image: url('../assets/images/headway-537308-unsplash-1380x703.jpg');
        
    }
    div.ax-secondary-post{
        width: calc(25% - 1rem);
        @include bgGradientToBottomRight($primaryColor , $primaryLightColor)
    }
</style>