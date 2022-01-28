<template>
  <div id="app">
    <header-box :buttons=nav />
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
  },

   data() {
        return {
            // NAV BUTTONS LIST
            nav: [
                {
                    id: '6qbpIDZVFg',
                    label: 'CHARACTERS',
                    url: '/characters',
                },
                {
                    id: 'oJOxo2iGa2',
                    label: 'COMICS',
                    url: '/comics',
                },
                {
                    id: 'MWAYK5tV6r',
                    label: 'MOVIES',
                    url: '/movies',
                },
                {
                    id: '2LbIce1R16',
                    label: 'TV',
                    url: '/tv',
                },
                {
                    id: 'k3Xoe1QWOr',
                    label: 'GAMES',
                    url: '/games',
                },
                {
                    id: 'SUyyRLeuVp',
                    label: 'COLLECTIBLES',
                    url: '/collectibles',
                },
                {
                    id: 'OqtshmcL5N',
                    label: 'VIDEOS',
                    url: '/videos',
                },
                {
                    id: 'oXT0PS1eQv',
                    label: 'FANS',
                    url: '/fans',
                },
                {
                    id: 'J6THQlVUFh',
                    label: 'NEWS',
                    url: '/news',
                },
                {
                    id: 'ZLepkzSQL5',
                    label: 'SHOP',
                    url: '/shop',
                },
            ],
        }
    }
}
</script>

<style lang="scss">
@import './style/main.scss';
</style>
