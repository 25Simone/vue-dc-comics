<template>
<div class="container">
    <div class="card">
        <div class="card-image">
            <img :src='thumb' alt="">
        </div>
        <p>{{}}</p>
    </div>
</div>
</template>

<script>
export default {
    name:'Card',
    props: {
        thumb: String,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';
.card{
    width: calc(100% / 6);
    padding: 10px;
}
</style>