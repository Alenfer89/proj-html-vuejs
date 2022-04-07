<template>
    <section class="container">
        <div class="row">
            <div class="col-12 d-flex justify-content-between align-items-center py-4">
                <div class="ax-img-wrapper">
                    <img src="../../assets/images/white-logo-2.png" alt="Phlox Corporate Logo" >
                </div>
                <nav class="d-flex justify-content-center align-items-center">
                    <ul class="mb-0">
                        <li class="text-capitalize px-2 d-inline-block"
                        v-for='(element, index) in sections'
                        :key='index'>
                            <a href=""> {{ element.name }} </a>
                        </li>
                    </ul>
                    <button class="ms-4">Sign-In</button>
                </nav>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'HeaderNav',
    data: function(){
        return{
            sections:[
                {
                    name: "home",
                    ref: "",
                    active: true
                },
                {
                    name: "about",
                    ref: "",
                    active: false
                },
                {
                    name: "services",
                    ref: "",
                    active: false
                },
                {
                    name: "blog",
                    ref: "",
                    active: false
                },
                {
                    name: "contact",
                    ref: "",
                    active: false
                },
                {
                    name: "portfolio",
                    ref: "",
                    active: false
                }
            ]
        }
    }
}
</script>

<style lang='scss' scoped>
@import '../../assets/styles/style.scss';
section{
    color: white;
    ul{
        list-style-type: none;
        a{
            text-decoration: none;
            color: white;
        }
    }
    button{
        @include betterButton;
        @include bgGradientLeftToRight($buttonPrimaryLight, $buttonPrimary);
    }
}
</style>