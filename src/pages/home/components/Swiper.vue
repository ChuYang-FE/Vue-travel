<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () { // ES6写法，直接用data()，ES5的话要 data:function()
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true// 允许循环轮播
      },
      swiperList: [
        {
          id: '0001',
          imgUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/e02cceb2dbbfcd2871cdb7531cf311f1.jpg_750x200_63d3d88b.jpg'
        },
        {
          id: '0002',
          imgUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/c36914f22fdb82d2b8878cbf6dddac98.jpg_750x200_4a63da4b.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.67%;
  background-color: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
