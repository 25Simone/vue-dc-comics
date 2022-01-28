<template>
<!-- CARD -->
    <div class="card" >
        <!-- CARD IMG -->
        <div class="card-image">
            <img class="thumb" :src='thumb' alt="card img">
            <!-- OVERLAY -->
            <div class="card-img-overlay">
                <img src="@/assets/dc-logo.png" alt="logo DC">
            </div>
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
    cursor: pointer;
    .card-image{
        position: relative;
        height: 170px;
        .thumb{
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
    .card-img-overlay{
        position: absolute;
        top: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, .5);
        display: none;
        >img{
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    }
    &:hover .card-img-overlay{
        display: block;
    }
}
</style>