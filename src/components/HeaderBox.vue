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
    data(){
        return {
            navButtonActive: false,
        }
    },
    props: {
       buttons: Array,
   },
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';
header{
    height: 110px;
    background: #fff;
    display: flex;
    justify-content: space-around;
    align-items: center;
    img{
        width: 85px;
    }
    nav{
        height: 100%;
        ul{
        height: 100%;
        display: flex;
        li{
            height: 100%;
            margin: 0 15px;
            font-size: 13px;
            font-weight: bold;
            display: flex;
            align-items: center;
            border-bottom: 3px solid transparent;
            &:hover{
                border-color: $blue-color;
            }
            &:hover a{
                color: $blue-color;
            }
            a{
                text-decoration: none;
                color: $text-secondary-color;
            }
        }
    }
}
    }
</style>