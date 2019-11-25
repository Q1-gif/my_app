<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <home-hot></home-hot>
    </div>
</template>

<script>
import HomeHeader from './componets/header'
import HomeSwiper from './componets/Swiper'
import HomeHot from './componets/Hot'
export default {
    name:'Home',
    components:{
        HomeHeader,
        HomeSwiper,
        HomeHot
    }
}
</script>

<style scoped>

</style>