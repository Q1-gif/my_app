<template>
    <div class="wrapper">
     <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide v-for='item of swiperList' :key='item.id'>
    <img class='swiper-img' :src='item.imgUrl' />
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default{
    name: 'HomeSwiper',
    data(){
        return{
            swiperOption:{
              pagination: '.swiper-pagination',
              loop:true
            },
            swiperList:[{
              id:'001',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/c8762210baff5ade1a3b2fe0ab914992.png_750x200_9bbb2f51.png'
            },{
              id:'002',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/1d8faa9f4d49b77ca1e61e2b478260f7.jpg_750x200_25cf76e2.jpg'
            },{
              id:'003',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/e7eac5a5e99e6517c61b953c0fece63b.jpg_750x200_4b701cf8.jpg'
            },{
              id:'004',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/6da1597f11456f5a42a1818ab3f6fa08.jpg_750x200_31b64c4a.jpg'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper   
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.66%
.swiper-img
  width: 100%
</style>