<template>
    <div>
        <div class="title">
            <span class="title-content">周末去哪儿</span>
        </div>
        <ul>
            <li v-for='item of weekList' :key='item.id'>
                <div class="week-img">
                    <img class="week-img-content" :src="item.imgUrl">
                </div>
                    <p class="tell">{{item.tell}}</p>
                    <p class="desc">{{item.desc}}</p>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'HomeWeek',
    data(){
        return{
            weekList:[{
                id:'001',
                imgUrl:'http://img1.qunarzz.com/sight/source/1711/2b/d4ebbd8337f1ac.jpg_r_640x214_2d4332c1.jpg',
                tell:'湖南泡汤圣地',
                desc:'山谷幽深，泉水潺潺，宜人的自然风光，怡人的田园景...'
            },{
                id:'002',
                imgUrl:'http://img1.qunarzz.com/sight/source/1509/3a/e163a8e32517d9.jpg_r_640x214_4fd882d3.jpg',
                tell:'边城秋色',
                desc:'不得不看的边城秋日之美'
            },{
                id:'003',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/88/8d3b492ebf0b16.jpg_r_640x214_7b3a281d.jpg',
                tell:'邂逅凤凰城',
                desc:'凤凰古城，一个古老而神秘的地方，风景秀丽，历史悠久...'
            },{
                id:'004',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/b4/71c01c98139cf.jpg_r_640x214_30bac495.jpg',
                tell:'亲身体验人间仙境',
                desc:'天桥天地，绝壁高崖之间的高台，台下深不见底的山涧...'
            },{
                id:'005',
                imgUrl:'http://img1.qunarzz.com/sight/source/1812/1e/131ba1bc67be3e.jpg_r_640x214_edd2705d.jpg',
                tell:'株洲必打卡',
                desc:'亲身体验株洲当地人最爱的去处'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.title
  margin .2rem
.week-img
  overflow hidden
  height 24%
  .week-img-content
    width 100%
.tell
  margin .2rem
.desc
  margin .2rem
  color #777
  font-size .08rem
</style>