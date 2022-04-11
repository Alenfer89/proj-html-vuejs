<template>
    <nav>
        <div class="container">
            <div class="row">
                <div class="col-12 d-flex justify-content-between align-items-center py-5">
                    <p class="m-0">
                        © 2022 phlox. All rights reserved.
                    </p>
                    <div>
                        <i class="fa-brands fa-instagram"></i>
                        <i class="fa-brands fa-linkedin-in"></i>
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                </div>
            </div>
        </div>
        
    </nav>
</template>

<script>
export default {
    name: 'BottomFooter'
}
</script>

<style lang='scss' scoped>
@import '../../assets/styles/style.scss';

nav{
    border-top: 1px solid rgba(255, 255, 255, 0.5);
    i{
        color: white;
        display: inline-block;
        margin-left: 3rem;
    }
}

</style>