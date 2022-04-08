<template>
    <div class="ax-card d-inline-block position-relative">
        <div class="ax-card-img-wrapper position-absolute p-2 ax-rounded">
            <img :src="require(`../assets/images/${service.image}`)" :alt="service.title" class="img-fluid">
        </div>
        <div class="ax-card-text text-center ax-rounded">
            <h4 class="ax-bold mb-4"> {{ service.title }} </h4>
            <p> {{ service.text }} </p>
        </div>
        <button class="ax-card-button position-absolute">--></button>
    </div>
</template>

<script>
export default {
    name: 'SingleServiceCard',
    props:['service']
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';
div.ax-card{
    width: calc(100% /4);

    div.ax-card-img-wrapper{
        top: 0;
        left: 50%;
        width: 50%;
        transform: translate(-50%, -50%);
        z-index: 1;
        background-color: white;
        img{
            object-fit: contain;
        }
    }
    &:hover div.ax-card-img-wrapper{
        box-shadow: 0 0 2rem 0 rgba(0, 0, 0, 0.495);
    }

    div.ax-card-text{
        padding: 10rem 2rem 4rem 2rem;
    }
    &:hover div.ax-card-text{
        color: white;
        @include bgGradientTopToBottom ($primaryLightColor, $primaryColor);
    }

    .ax-rounded{
        border-radius: 2rem;
    }

    button{
        display: none;
        width: 3rem;
        height: 3rem;
        line-height: 3rem;
        color: white;
        border: transparent;
        border-radius: 50%;
        left: 50%;
        bottom: 0;
        transform: translate(-50%, 50%);
        @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor);
    }
    &:hover button{
        display: inline-block;
    }
}


</style>