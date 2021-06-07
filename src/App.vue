<template>
  <div id="app">
    <Header />
    <Main />
    <Banner />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Banner from './components/Banner.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Banner,
    Footer
  }
}
</script>

<style lang="scss">
  @import "./style/global.scss";
</style>
