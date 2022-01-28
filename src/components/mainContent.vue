<template>
    <main>
        <div class="container">
            <div class="button current-series-button">CURRENT SERIES</div>
            <!-- CARDS -->
            <div class="container cards-container">
                <card-box
                v-for='(card, index) in cards'
                :key='index'
                :thumb='card.thumb'
                :series='card.series'
                :type='card.type'
                :price='card.price'
                />
            </div>
            
        </div>
        <div id="load-more-section">
            <div class="button">LOAD MORE</div>
        </div>
    </main>
</template>

<script>
import comicsList from '@/jsons/comicsList.json'
import CardBox from './CardBox.vue'
export default {
    name: 'Main',
    components: {
        CardBox,
    },
    data(){
        return {
            cards: comicsList,
        }
    }
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
main{
    width: 100%;
    background: #1c1c1c;
    position: relative;
    .button.current-series-button{
        position: absolute;
        top: -25px;
    }
    .cards-container{
        display: flex;
        flex-wrap: wrap;
        padding: 30px;
    }
    #load-more-section{
        padding: 30px;
        display: flex;
        justify-content: center;
    }
}
</style>