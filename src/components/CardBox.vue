<template>
    <div class="card" >
        <div class="card-image">
            <img :src='thumb' alt="card img">
        </div>
        <h4>{{series.toUpperCase()}}</h4>
    </div>
</template>

<script>
export default {
    name:'Card',
    props: {
        thumb: String,
        series: String,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';
.card{
    width: calc(100% / 6);
    padding: 10px;
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
    }
}
</style>