<template>
  <div id="app">
    <header>
      <HeaderNav />
      <Jumbotron />
    </header>
    <main>
      <h1>main</h1>
    </main>
    <footer>
      <Footer />
    </footer>
  </div>
</template>

<script>
import HeaderNav from './components/HeaderSubComps/HeaderNav.vue';
import Jumbotron from './components/HeaderSubComps/Jumbotron.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    HeaderNav,
    Jumbotron,
    Footer
  }
}
</script>

<style lang="scss">
@import './assets/styles/style.scss';

header{
  height: 100vh;
  @include bgGradientTopToBottom($primaryLightColor, $primaryColor)
}

</style>
