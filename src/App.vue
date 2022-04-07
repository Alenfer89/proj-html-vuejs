<template>
  <div id="app">
    <Header />
    <main>
      <h1>main</h1>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
@import './assets/styles/style.scss';

</style>
