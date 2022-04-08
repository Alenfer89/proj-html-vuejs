<template>
  <div id="app">
    <header>
      <HeaderNav />
      <Jumbotron />
    </header>

    <main>
      <Services />
      <Businness />
    </main>

    <footer>

    </footer>
  </div>
</template>

<script>
import HeaderNav from './components/HeaderSubComps/HeaderNav.vue';
import Jumbotron from './components/HeaderSubComps/Jumbotron.vue';
import Services from './components/SectionServices.vue';
import Businness from './components/SectionBusinness.vue';

export default {
  name: 'App',
  components: {
    HeaderNav,
    Jumbotron,
    Services,
    Businness,
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
