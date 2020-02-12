<template>
  <div id="app">
    <Navigation/>
    <Header/>
    <Main/>
    <Footer/>
    <Popup/>
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Popup from './components/Popup.vue'

export default {
  name: 'App',
  components: {
    Navigation,
    Header,
    Main,
    Footer,
    Popup
  }
}
</script>

<style lang="scss">
@import "assets/sass/main";
</style>
