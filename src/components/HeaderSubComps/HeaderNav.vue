<template>
    <nav class="container">
        <div class="row">
            <div class="col-12 d-flex justify-content-between align-items-center py-4">
                <!-- logo -->
                <div class="ax-img-wrapper">
                    <img src="../../assets/images/white-logo-2.png" alt="Phlox Corporate Logo" >
                </div>
                <!-- nav bar with referrals to sections -->
                <div class="d-flex justify-content-center align-items-center">
                    <ul class="mb-0">
                        <li class="text-capitalize px-2 d-inline-block"
                        v-for='(section, index) in sections'
                        :key='index'
                        @click='setActiveLink(index)'>
                        <!-- link ref to add with js -->
                            <a href="#" :class="(section.active)? 'active' : '' "> {{ section.name }} </a>
                        </li>
                    </ul>
                    <button class="ms-4">Sign-In</button>
                </div>
            </div>
        </div>
    </nav>
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
    },
    methods:{
        setActiveLink(activeIndex){
            this.sections.forEach((element, index) => {
                if(activeIndex === index){
                    element.active = true;
                } else{
                    element.active = false;
                }
            });
        }
    }
}
</script>

<style lang='scss' scoped>
@import '../../assets/styles/style.scss';
nav{
    color: white;
    ul{
        list-style-type: none;
        a{
            text-decoration: none;
            color: white;
            &:hover{
                color: $secondaryLightColor;
            }
        }
        a.active{
            color: $secondaryColor;
        }
    }
    button{
        @include betterButton;
        @include bgGradientLeftToRight($buttonPrimaryLight, $buttonPrimary);
    }
}
</style>