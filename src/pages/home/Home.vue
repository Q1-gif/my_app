<template>
    <div>
        <home-header :city='city'></home-header>
        <home-swiper :list='swiperList'></home-swiper>
        <home-icons :list='iconList'></home-icons>
        <home-hot :list='hotList'></home-hot>
        <home-Liked :list='likedList'></home-Liked>
        <home-Week :list='weekList'></home-Week>
    </div>
</template>

<script>
import HomeHeader from './componets/header'
import HomeSwiper from './componets/Swiper'
import HomeIcons from './componets/Icons'
import HomeHot from './componets/Hot'
import HomeLiked from './componets/Liked'
import HomeWeek from './componets/Week'
import axios from 'axios'
export default {
    name:'Home',
    components:{
        HomeHeader,
        HomeSwiper,
        HomeIcons,
        HomeHot,
        HomeLiked,
        HomeWeek
    },
    data(){
        return{
            city:'',
            swiperList:[],
            iconList:[],
            hotList:[],
            likedList:[],
            weekList:[]
        }
    },
    methods:{
        getHomeInfo(){
            axios.get('/api/index.json').then(this.getHomeInfoSucc)
        },
        getHomeInfoSucc(res){
            res=res.data
            if(res.ret && res.data){
                const data=res.data
                this.city=data.city
                this.swiperList=data.swiperList
                this.iconList=data.iconList
                this.hotList=data.hotList
                this.likedList=data.likedList
                this.weekList=data.weekList
            }
        }
    },
    mounted(){
        this.getHomeInfo()
    }
}
</script>

<style scoped>

</style>