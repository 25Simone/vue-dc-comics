<template>
<!-- CARD -->
    <div class="card" >
        <!-- CARD IMG -->
        <div class="card-image">
            <img :src='thumb' alt="card img">
        </div>
        <h4>{{series.toUpperCase()}}</h4>
        <!-- CARD TXT -->
        <p>
            {{type}}
            <br />
            {{price}}
        </p>
    </div>
</template>

<script>
export default {
    name:'Card',
    props: {
        thumb: String,
        series: String,
        type: String,
        price: String,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.card{
    width: calc(100% / 6);
    padding: 15px;
    .card-image{
        height: 170px;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }
    h4{
        color: $text-primary-color;
        font-weight: 400;
        margin-top: 15px;
    }
    p{
        color: #ccc;
    }
}
</style>