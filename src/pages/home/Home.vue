<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
    </div>
</template>

<script>
import HomeHeader from './componets/header'
import Homeswiper from './componets/Swiper'
export default {
    name:'Home',
    components:{
        HomeHeader,
        Homeswiper
    }
}
</script>

<style scoped>

</style>