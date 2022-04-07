<template>
    <header>
        <h1>header</h1>
        <HeaderNav />
        <Jumbotron />
    </header>
</template>

<script>
import HeaderNav from './HeaderSubComps/HeaderNav.vue';
import Jumbotron from './HeaderSubComps/Jumbotron.vue';

export default {
    name: 'IndexHeader',
    components: {
        HeaderNav,
        Jumbotron
    }
}
</script>

<style>

</style>