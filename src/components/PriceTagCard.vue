<template>
    <div class="ax-price-tag  position-relative shadow">
        <div class="ax-text-wrapper text-center d-flex flex-column justify-content-between align-items-center p-5">
            <div>
                <h3 class="text-capitalize"> {{ tag.name }} </h3>
                <p class="text-uppercase"> {{ tag.type }} </p>
            </div>
            <div>
                <p class="d-flex justify-content-between">
                    <span>$</span>
                    <span></span>
                </p>
                <h1 class="ax-tag-number"> {{ tag.price }} </h1>
                <p>per month</p>
            </div>
            <ul class="p-0 m-0">
                <li class="text-capitalize"
                v-for='(specific, index) in specificsList'
                :key='index'>
                <span class="ax-bold"> {{ specific.title }} </span>
                <span> {{ specific.description }} </span>
                </li>
            </ul>
            <button :class="(index % 2 == 0) ? 'ax-odd-button' : 'ax-even-button' ">
                <span class="me-5">order now</span> -->
            </button>
        </div>
        <span class="ax-bg-pricing position-absolute text-end">
            {{ tag.price }}
        </span>
        
    </div>
    
</template>

<script>
export default {
    name: 'PriceTagCard',
    data: function(){
        return {
            specificsList:[
                {
                    title:'creative',
                    description: ' design enabled'
                },
                {
                    title:'vibrant',
                    description: 'color usage'
                },
                {
                    title:'eye',
                    description: 'catching design'
                },
                {
                    title:'extreme',
                    description: 'typography'
                },
                {
                    title:'exceptional',
                    description: 'design'
                }
            ]
        }
    },
    props:['tag', 'index'],
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';

div.ax-price-tag{
    width: calc((100% / 3) - 1rem);
    height: 600px;
    background-color: white;
    border-radius: 2rem;

    div.ax-text-wrapper{
        height: 100%;
        position: relative;
        z-index: 2;

        .ax-tag-number{
            font-weight: bold;
            font-size: 5rem;
        }
        ul{
            list-style-type: none;
        }
    }
    span.ax-bg-pricing{
        z-index: 1;
        top: 0;
        right: 0;
        line-height: 10rem;
        font-size: 14rem;
        font-weight: bold;
        opacity: .1;
    }
    button.ax-odd-button{
        @include betterButton($secondaryLightColor);
        @include bgGradientLeftToRight ($secondaryColor, $secondaryLightColor);
        color: white;
    }
    button.ax-even-button{
        @include betterButton(white);
        @include bgGradientLeftToRight (white, white);
        color: $secondaryLightColor;
    }
    
    
}
</style>