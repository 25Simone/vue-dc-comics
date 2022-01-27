<template>
    <header>
        <div id="logo">
            <img src="@/assets/dc-logo.png" alt="logo Dc Comics">
        </div>
        <nav>
            <ul>
                <li>CHARACTERS</li>
                <li>COMICS</li>
                <li>MOVIES</li>
                <li>TV</li>
                <li>GAMES</li>
                <li>COLLECTIBLES</li>
                <li>VIDEOS</li>
                <li>FANS</li>
                <li>NEWS</li>
                <li>SHOP</li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    
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
        color: $text-secondary-color;
        li{
            padding: 15px;
            font-size: 15px;
        }
    }
}
</style>