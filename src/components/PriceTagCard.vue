<template>
    <div class="ax-price-tag p-5 text-center d-flex flex-column justify-content-between align-items-center">
        <div>
            <h3>ciao</h3>
            <p>type</p>
        </div>
        <div>
            <p class="d-flex justify-content-between">
                <span>$</span>
                <span></span>
            </p>
            <h1>40</h1>
            <p>per month</p>
        </div>
        <div>
            <ul>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>
        </div>
        <button><span class="me-5">order now</span> --></button>
    </div>
    
</template>

<script>
export default {
    name: 'PriceTagCard',
    data: function(){
        return {

        }
    },
    props:[],
}
</script>

<style lang='scss' scoped>
@import '../assets/styles/style.scss';

div.ax-price-tag{
    width: 32%;
    height: 600px;
    background-color: aqua;
    border-radius: 2rem;
}
</style>