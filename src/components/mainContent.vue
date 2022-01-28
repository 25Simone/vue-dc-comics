<template>
    <main>
        <div class="container">
            <div class="button">CURRENT SERIES</div>
            <div class="container cards-container">
            <card-box
            v-for='(card, index) in cards'
            :key='index'
            :thumb='card.thumb'
            :series='card.series'
            />
            </div>
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
    height: 700px;
    background: #1c1c1c;
    position: relative;
    .button{
        color: #fff;
        font-size: 25px;
        font-weight: bold;
        padding: 10px 25px;
        position: absolute;
        top: -25px;
        display: inline-block;
        background: $blue-color;
    }
    .cards-container{
        display: flex;
        flex-wrap: wrap;
        padding: 30px;
    }
}
</style>