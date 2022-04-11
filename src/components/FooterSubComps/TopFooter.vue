<template>
    <section class="position-relative mt-5">
        <div id="footer-tag" class="position-relative">
            <div class="container">
                <div class="row">
                    <div class="col d-flex justify-content-between align-items-center p-5 w-50">
                        <div>
                            <h1 class="text-capitalize ax-bold">we offer awesome services</h1>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                        <div class="ax-input-wrapper p-2 ms-5 text-end bg-white d-flex">
                            <input type="text" class="flex-grow-1" placeholder="Enter Your Email Address">
                            <button class="" type="button">Subscribe</button>
                        </div>
                        
                    </div>
                </div>
            </div>
        </div>
        
        <div class="container">
            <div class="row row-col-4">
                <div class="col">
                    <div class="mb-4">
                        <img src="../../assets/images/white-logo-2.png" alt="Company Logo">
                    </div>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tenetur ut quae culpa laudantium? Natus sequi cupiditate</p>
                </div>
                <div class="col px-5">
                    <h4 class="ax-bold mb-4"> Quick Links </h4>
                    <ul class="p-0 m-0">
                        <li v-for='(element,index) in quickLinksList' :key="index">
                            <a href=""> {{ element }} </a>
                        </li>
                    </ul>
                </div>
                <div class="col px-5">
                    <h4 class="ax-bold mb-4"> Resources </h4>
                    <ul class="p-0 m-0">
                        <li class="text-end" v-for='(element,index) in resourcesList' :key="index">
                            <a href=""> {{ element }} </a>
                        </li>
                    </ul>
                </div>
                <div class="col px-5">
                    <h4 class="ax-bold mb-4"> Contact Us </h4>
                    <ul class="p-0 m-0">
                        <li v-for='(element,index) in contactsList' :key="index">
                            <a href="">
                                <span class="ax-bold"> {{ element.type }} </span>
                                : {{ element.text }}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name:'TopFooter',
    data: function(){
        return{
            quickLinksList:['Services', 'Contact', 'Blog'],
            resourcesList:['Art Design', 'Computer', 'IT News', 'Netwroking', 'Net Security'],
            contactsList:[
                {
                    type:'Address',
                    text: 'Patricia C. Amedee 4401 Waldeck Street Grapevine Nashville, Tx 76051'
                },
                {
                    type: 'Phone',
                    text: '+99 (0) 101 0000 888'
                },
                {
                    type:'Email',
                    text: 'Info@yourdomain.com'
                }
            ],
        }
    }
}
</script>

<style lang='scss' scoped>
@import '../../assets/styles/style.scss';

div#footer-tag{
    top: 0;
    left: 0;
    transform: translateY(-50%);
    
    div.col{
        @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor);
        height: 12rem;
        border-radius: 2rem;
    }
    div.ax-input-wrapper{
        border-radius: 50rem;
        width: 40%;
    }
    input{
        border: none;
        border-radius: 50rem;
        &:focus{
            outline: none;
        }
    }
    button{
        @include betterButton($secondaryLightColor);
        @include bgGradientLeftToRight ($buttonPrimaryLight , $buttonPrimary);
        &:hover{
            @include bgGradientLeftToRight ($secondaryColor , $secondaryLightColor);
        }
    }
}
h4{
    color: white;
}
ul{
        list-style-type: none;
        li{
            a{
                text-decoration: none;
                color: rgba(255, 255, 255, 0.5);
                &:hover{
                    color: white;
                }
            }
        }
    }

</style>