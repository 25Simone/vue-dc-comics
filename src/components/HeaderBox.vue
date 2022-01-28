<template>
    <header>
        <div id="logo">
            <img src="@/assets/dc-logo.png" alt="logo Dc Comics">
        </div>
        <nav>
            <ul>
                <li v-for='button in buttons' :key='button.id'>
                    <a :href="button.url">{{button.label}}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
   props: {
       buttons: Array,
   }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';
header{
    background: #fff;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 10px;
    img{
        width: 85px;
    }
    ul{
        display: flex;
        li{
            margin: 0 15px;
            font-size: 13px;
            font-weight: bold;
            a{
                text-decoration: none;
                color: $text-secondary-color;
            }
        }
    }
}
</style>