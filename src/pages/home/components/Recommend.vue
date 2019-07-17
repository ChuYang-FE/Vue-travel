<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img" :src="item.imgUrl">
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>   
</template>

<script>
export default {
    name: 'HomeRecommend',
    data () {
        return {
            recommendList:[{
            id:'0001',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_250x250_30e841af.jpg',
            title:'长隆野生动物世界',
            desc:'长隆野生动物世界长隆野生动物世界长隆野生动物世界'
            }, {
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1707/d8/d89ab1a9b2ab355ba3.img.jpg_250x250_dc7083b2.jpg',
            title:'长隆水上乐园',
            desc:'长隆水上乐园长隆水上乐园长隆水上乐园长隆水上乐园'
            }, {
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1707/88/889ae02b07140066a3.img.jpg_250x250_d4ca7f0a.jpg',
            title:'长隆欢乐世界',
            desc:'长隆欢乐世界长隆欢乐世界长隆欢乐世界长隆欢乐世界'
            }]
            
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
    .title
        margin-top .2rem
        line-height .8rem
        background #eee
        text-indent .2rem 
    .item
        overflow hidden
        display flex
        height 1.9rem
        .item-img
            width 1.7rem
            height 1.7rem
            padding .1rem
        .item-info
            flex 1
            padding .1rem   
            min-width 0
            .item-title
                ellipsis()
                line-height .54rem
                font-size .32rem
            .item-desc 
                ellipsis()
                line-height .4rem
                color #ccc
            .item-button
                line-height .44rem
                margin-top .16rem
                background #ff9300
                padding 0 .2rem
                border-radius .06rem    
                color #fff
</style>
