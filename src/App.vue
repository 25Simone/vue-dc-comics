<template>
  <div id="app">
    <header-box />
    <jumbotron-box />
    <main-content />
    <footer-app />
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'
import JumbotronBox from './components/JumbotronBox.vue'
import MainContent from './components/MainContent.vue'
import FooterApp from './components/FooterApp'
export default {
  name: 'App',
  components: {
    HeaderBox,
    JumbotronBox,
    MainContent,
    FooterApp,
  }
}
</script>

<style lang="scss">
@import './style/main.scss';
</style>
