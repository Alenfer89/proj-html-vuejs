<template>
  <div id="app">
    <header>
      <HeaderNav />
      <Jumbotron />
    </header>

    <main>
      <Services />
      <Businness />
      <Portfolio />
      <Pricing />
      <Blog />
      <Testimonial />
    </main>

    <footer>
      <TopFooter />
      <BotFooter />
    </footer>
  </div>
</template>

<script>
import HeaderNav from './components/HeaderSubComps/HeaderNav.vue';
import Jumbotron from './components/HeaderSubComps/Jumbotron.vue';
import Services from './components/SectionServices.vue';
import Businness from './components/SectionBusinness.vue';
import Portfolio from './components/SectionPortfolio.vue';
import Pricing from './components/SectionPricing.vue';
import Blog from './components/SectionBlog.vue';
import Testimonial from './components/SectionTestimonial.vue';
import TopFooter from './components/FooterSubComps/TopFooter.vue';
import BotFooter from './components/FooterSubComps/BotFooter.vue';


export default {
  name: 'App',
  components: {
    HeaderNav,
    Jumbotron,
    Services,
    Businness,
    Portfolio,
    Pricing,
    Blog,
    Testimonial,
    TopFooter,
    BotFooter
  }
}
</script>

<style lang="scss">
@import './assets/styles/style.scss';

header{
  height: 100vh;
  @include bgGradientTopToBottom($primaryLightColor, $primaryColor)
}
footer{
  color: rgba(255, 255, 255, 0.5);
  @include bgGradientTopToBottom($primaryLightColor, $primaryColor)
}


</style>
